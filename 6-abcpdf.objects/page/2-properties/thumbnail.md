# Thumbnail Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp PixMap ``` [Visual Basic] `PixMap` | n/a | No | The Thumbnail for the page | 

## Notes

Each page can have a thumbnail image for quick preview purposes. This property allows to access such a thumbnail if it exists, or to assign such a thumbnail to a page if it does not.

## Example

This example shows how to create and embed thumbnails in a PDF document.

[C#]

```csharp
using var doc = new Doc();
using var src = new Doc();
doc.Read(Server.MapPath("spaceshuttle.pdf"));
doc.Rendering.DotsPerInch = 18;
var pages = doc.ObjectSoup.Catalog.Pages.GetPageArrayAll();
foreach (var page in pages) {
  doc.Page = page.ID;
  using (var xi = XImage.FromData(doc.Rendering.GetData(".jpg"), null))
    page.Thumbnail = PixMap.FromXImage(doc.ObjectSoup, xi);
}
doc.Save(Server.MapPath("embedthumbnails.pdf"));
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc(), srcDoc As New Doc()
  doc.Read(Server.MapPath("spaceshuttle.pdf"))
  doc.Rendering.DotsPerInch = 18
  Dim pages As Page() = doc.ObjectSoup.Catalog.Pages.GetPageArrayAll()
  For Each page As Page In pages
    doc.Page = page.ID
    Using xi As XImage = XImage.FromData(doc.Rendering.GetData(".jpg"), Nothing)
      page.Thumbnail = PixMap.FromXImage(doc.ObjectSoup, xi)
    End Using
  Next
  doc.Save(Server.MapPath("embedthumbnails.pdf"))
End Using
```