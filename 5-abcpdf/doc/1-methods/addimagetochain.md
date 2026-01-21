# AddImageToChain Function

Adds a new page from a paged HTML or PostScript render.

## Syntax

**[C#]**

```csharp
int AddImageToChain(int id)
```

<span class=language>[Visual
            Basic]</span>  
`Function AddImageToChain(id As Integer) As Integer``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| id | The ID of the previous object in the chain. | 
| return | The ID of the newly added object. | 

## Notes

Some web pages are too large to fit on one PDF page.

To split a web page across multiple PDF pages you need to call [AddImageUrl](addimageurl.md) or [AddImageHtml](addimageurl.md) to render the first page. The ID returned from these calls represents the head of the chain.

To add subsequent pages to the chain you need to make calls to AddImageToChain passing in the previous image from the chain each time.

As well as using chaining to split web pages across multiple PDF pages you can also use it to split your web pages across multiple columns within a page. You can even split your chain to generate multiple copies of the same page.

More information can be found in the [HTML / CSS Rendering](../../../3-concepts/g-htmlrender.md) section of the documentation.

Similarly some PostScript (PS) files contain more than one page of content.

To split a PS file across multiple PDF pages you need to call [AddImageFile](addimagefile.md) or [AddImageData](addimagedata.md) to render the first page. The ID returned from these calls represents the head of the chain.

To add subsequent pages to the chain you need to make calls to AddImageToChain passing in the previous image from the chain each time.

## Example

This example shows how to import an HTML page into a multi-page PDF document.

We first create a [Doc](../default.md) object and inset the edges a little so that the HTML will appear in the middle of the page.

[C#]

```csharp
using var doc = new Doc();
doc.Rect.Inset(72, 144);
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc()
  doc.Rect.Inset(72, 144)
```

We add the first page of HTML. We save the returned ID as this will be used to add subsequent pages.

[C#]

```csharp
int id = doc.AddImageUrl("http://www.yahoo.com/");
```

<span class=language>[Visual Basic]</span>
```vbnet
Dim theID As Integer
theID = doc.AddImageUrl("http://www.yahoo.com/")
```

We now chain subsequent pages together. We stop when we reach a page which wasn't truncated.

[C#]

```csharp
while (true) {
  doc.FrameRect();
  if (!doc.Chainable(id))
    break;
  doc.Page = doc.AddPage();
  id = doc.AddImageToChain(id);
}
```

<span class=language>[Visual Basic]</span>
```vbnet
While True
  doc.FrameRect()
  If Not doc.Chainable(theID) Then
    Exit While
  End If
  doc.Page = doc.AddPage()
  theID = doc.AddImageToChain(theID)
End While
```

After adding the pages we can flatten them. We can't do this until after the pages have been added because flattening will invalidate our previous ID and break the chain.

[C#]

```csharp
for (int i = 1; i <= doc.PageCount; i++) {
  doc.PageNumber = i;
  doc.Flatten();
}
```

<span class=language>[Visual Basic]</span>
```vbnet
Dim i As Integer = 1
While i <= doc.PageCount
  doc.PageNumber = i
  doc.Flatten()
  System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1)
End While
```

Finally we save.

[C#]

```csharp
doc.Save(Server.MapPath("paged_html.pdf"));
```

<span class=language>[Visual
            Basic]</span>
```vbnet
doc.Save(Server.MapPath("paged_html.pdf"))
End Using
```

We get the following output.

![](../../../images/pdf/paged_html.pdf.png)
                paged_html.pdf [Page 1]![](../../../images/pdf/paged_html.pdf2.png)
                paged_html.pdf [Page 2]