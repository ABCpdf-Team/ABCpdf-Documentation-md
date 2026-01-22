# Save Function

Renders and saves a page.

## Syntax

[C#]

```csharp
void Save(string path)
```

[Visual Basic]

```vb
Sub Save(path As String)
```

## Params

| **Name** | **Description** |
| --- | --- |
| path | The destination file path. |

## Notes

Renders and saves a page.

The page and rendering options which will be used are those which were current at the time the RenderOperation was created.

This method is similar in functionality to [XRendering.Save](5-abcpdf/xrendering/1-methods/save.md), but allows safe multithreaded use.

You can create multiple different RenderOperations to render different pages, or indeed the same page, of a document. Each RenderOperation may live on a different thread. So the typical process is to create multiple RenderOperations on the main thread and then parcel them off to different threads which will call the Save method. The only restriction is that the pages in question must not be modified while being rendered.

Every [ProcessingObject](1-operation/3-events/1-processingobject.md) event is followed by a corresponding [ProcessedObject](1-operation/3-events/2-processedobject.md), event with the same source type. The PageContent [ProcessedObject](1-operation/3-events/2-processedobject.md) event will be the last event received, in that all the page objects events are sandwiched between a PageContent processing and processed events. Similarly for form streams, all the form objects events are sandwiched between a Stream processing and processed events, which in turn are sandwiched between the FormXObject processing and processed events.

Any event property or event Info property not mentioned here will be ignored.

## Example

Here we render all the pages of the doc using 10 threads at a time. We alternate rendering format between jpg and tiff. We also alternate resolution between 150 and 300 dpi. Note how the RenderingOperation is created in the constructor of TheRenderingWorker. This is because at this point a copy of the rendering options is made. Had we created the RenderingOperation in DoWork, we would have picked up only the last doc.Rendering.DotsPerInch, because the threads are started in the following loop. Also note how we dispose the operation in DoWork, to release resources stored on the native side (the copy of the rendering options basically).

[C#]

```csharp
using var doc = new Doc();
doc.Read(Server.MapPath("spaceshuttle.pdf"));
string[] xts = { ".jpg", ".tif" };
int[] dpis = { 150, 300 };
var threads = new Thread[10];
int pageNum = 1, pageCount = doc.PageCount;
while (pageNum <= pageCount) {
  int count = 0;
  while (count < threads.Length && pageNum <= pageCount) {
    doc.Rendering.DotsPerInch = dpis[(pageNum - 1) % 2];
    doc.PageNumber = pageNum;
    string path = Server.MapPath($"ABCpdf{pageNum}{xts[(pageNum - 1) % 2]}");


    threads[count] = new Thread(new RenderingWorker(doc, path).DoWork);
    ++count;
    ++pageNum;
  }
  for (int i = 0; i < count; ++i)
    threads[i].Start();
  for (int i = 0; i < count; ++i)
    threads[i].Join();
}
```

[Visual Basic]

```vb
Using doc As New Doc()
  doc.Read(Server.MapPath("spaceshuttle.pdf"))
  Dim theExts As String() = {".jpg", ".tif"}
  Dim theDpis As Integer() = {150, 300}
  Dim threadList As Thread() = New Thread(9) {}
  Dim pageNum As Integer = 1, pageCount As Integer = doc.PageCount
  While pageNum <= pageCount
    Dim count As Integer = 0
    While count < threadList.Length AndAlso pageNum <= pageCount
      doc.Rendering.DotsPerInch = theDpis((pageNum - 1) Mod 2)
      doc.PageNumber = pageNum
      Dim path As String = Server.MapPath($"ABCpdf{pageNum}{theExts[(pageNum - 1) % 2]}")


      threadList(count) = New Thread(New RenderingWorker(doc, path).DoWork)
      System.Threading.Interlocked.Increment(count)
      System.Threading.Interlocked.Increment(pageNum)
    End While
    Dim i As Integer = 0
    While i < count
      threadList(i).Start()
      System.Threading.Interlocked.Increment(i)
    End While
    Dim i As Integer = 0
    While i < count
      threadList(i).Join()
      System.Threading.Interlocked.Increment(i)
    End While
  End While
End Using
```

