---
title: "save"
css: "abcpdf-docs.css"
---

|  |  | Save Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Renders and saves a page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Save(string path) ``` [Visual Basic] ``` Sub Save(path As String) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The destination file path. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Renders and saves a page. The page and rendering options which will be used are those which were current at the time the RenderOperation was created. This method is similar in functionality to XRendering.Save, but allows safe multithreaded use. You can create multiple different RenderOperations to render different pages, or indeed the same page, of a document. Each RenderOperation may live on a different thread. So the typical process is to create multiple RenderOperations on the main thread and then parcel them off to different threads which will call the Save method. The only restriction is that the pages in question must not be modified while being rendered. Furthermore, this method generates the following events, allowing fine tuning of the rendering operations: Before rendering begins, a ProcessingObject event of ProcessingSourceType.PageContent is generated. Set the event arguments' Cancel property to true to skip rendering altogether. When a PDF path stroking or filling operator is found in the page content, a ProcessingObject event of ProcessingSourceType.Path is generated. Set the event arguments' Cancel property to true to skip this object. The stream length and position can be retrieved via the StreamPosition and StreamLength properties. Set the stream position to null to skip the remaining of the stream. When a text PDF operator is found, a ProcessingObject event of ProcessingSourceType.Text is generated. The Unicode text can be retrieved in the Text property of the event Info property. the event cancel property to true to skip this object. The stream length and position can be retrieved via the StreamPosition and StreamLength properties. Set the stream position to null to skip the remaining of the stream. When a shading PDF operator is found, a ProcessingObject event of ProcessingSourceType.Shading is generated. The same comments of point 2 above apply, for skipping the object or retrieving/setting the stream position and length. When an image is found (inline or XObject), a ProcessingObject event of ProcessingSourceType.Image is generated. If the image is XObject, the indirect object can be retrieved via the event arguments' Object property. the event cancel property to true to skip this object. The stream length and position can be retrieved via the StreamPosition and StreamLength properties. Set the stream position to null to skip the remaining of the stream. When a Form XObject is found, a ProcessingObject event of ProcessingSourceType.FormXObject is generated. The indirect object can be retrieved via the event arguments' Object property. Set the event arguments' Cancel property to true to skip this object. The stream length and position can be retrieved via the StreamPosition and StreamLength properties. Set the stream position to null to skip the remaining of the stream. In addition, because Forms contain streams, a ProcessingObject event of ProcessingSourceType.Stream will follow. You can set the stream position to null to skip the stream at any time. That is events for the objects contained in the Form stream will be generated, as described in points 2 to 5. Setting the stream position to null for Form objects will skip the Form stream, not the entire page content. Every ProcessingObject event is followed by a corresponding ProcessedObject, event with the same source type. The PageContent ProcessedObject event will be the last event received, in that all the page objects events are sandwiched between a PageContent processing and processed events. Similarly for form streams, all the form objects events are sandwiched between a Stream processing and processed events, which in turn are sandwiched between the FormXObject processing and processed events. Any event property or event Info property not mentioned here will be ignored. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we render all the pages of the doc using 10 threads at a time. We alternate rendering format between jpg and tiff. We also alternate resolution between 150 and 300 dpi. Note how the RenderingOperation is created in the constructor of TheRenderingWorker. This is because at this point a copy of the rendering options is made. Had we created the RenderingOperation in DoWork, we would have picked up only the last doc.Rendering.DotsPerInch, because the threads are started in the following loop. Also note how we dispose the operation in DoWork, to release resources stored on the native side (the copy of the rendering options basically). [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("spaceshuttle.pdf")); string[] xts = { ".jpg", ".tif" }; int[] dpis = { 150, 300 }; var threads = new Thread[10]; int pageNum = 1, pageCount = doc.PageCount; while (pageNum [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("spaceshuttle.pdf")) Dim theExts As String() = {".jpg", ".tif"} Dim theDpis As Integer() = {150, 300} Dim threadList As Thread() = New Thread(9) {} Dim pageNum As Integer = 1, pageCount As Integer = doc.PageCount While pageNum [C#] ```csharp class RenderingWorker { private string mPath; private RenderOperation mOp; public RenderingWorker(Doc inDoc, string inPath) { mPath = inPath; mOp = new RenderOperation(inDoc); } public void DoWork() { mOp.Save(mPath); mOp.Dispose(); } } ``` [Visual Basic] ```vbnet Private Class RenderingWorker Private mPath As String Private mOp As RenderOperation Public Sub New(inDoc As Doc, inPath As String) mPath = inPath mOp = New RenderOperation(inDoc) End Sub Public Sub DoWork() mOp.Save(mPath) mOp.Dispose() End Sub End Class ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>