# GetBitmap Function

Get the PixMap image as a System.Drawing.Bitmap.

## Syntax

[C#]

```csharp
System.Drawing.Bitmap GetBitmap()
```

[Visual Basic]

```vb
Function GetBitmap() As System.Drawing.Bitmap
```

## Params

| **Name** | **Description** |
| --- | --- |
| return | The Bitmap containing the image. |

## Notes

Use this method to get the PixMap image as a System.Drawing.Bitmap.

You can then use this Bitmap for drawing to screen or for manipulation using System.Drawing routines.

ABCpdf tries to make a literal copy of the image contained in the PixMap, both to minimize color shifts and also for speed.

However because PDF images can contain many color spaces and bit depths that are unsupported by System.Drawing it may be necessary to change the color space or bit depth of the image.

In addition there are certain parameters such as decode arrays which may be used to modify the image before display. This method returns the image content as literally as possible which means decode arrays and alpha channels are not included.

Please note that some formats of Bitmaps are not usable for certain operations. In particular, indexed color bitmaps cannot be drawn on using the Graphics.FromImage method. For this reason if you are going to wish to draw on the returned Bitmap you should check the pixel format before use.

## Example

This example shows how to extract all the page thumbnails (if they exist) from a document. See also the PDFSurgeon example project for another example.

[C#]

```csharp
using var doc = new Doc();
using var src = new Doc();
doc.Read(Server.MapPath("embedthumbnails.pdf"));
doc.Rendering.DotsPerInch = 18;
var pages = doc.ObjectSoup.Catalog.Pages.GetPageArrayAll();
foreach (var page in pages) {
  if (page.Thumbnail == null)
    continue;
  using var bm = page.Thumbnail.GetBitmap();
  bm.Save($"embedthumbnails{page.Thumbnail.ID}.jpg");
}
```

[Visual Basic]

```vb
Using doc As New Doc(), srcDoc As New Doc()
  doc.Read(Server.MapPath("embedthumbnails.pdf"))
  doc.Rendering.DotsPerInch = 18
  Dim pages As Page() = doc.ObjectSoup.Catalog.Pages.GetPageArrayAll()
  For Each page As Page In pages
    If page.Thumbnail = Nothing Then
      Continue For
    End If
    Using bm As Bitmap = page.Thumbnail.GetBitmap()
      bm.Save($"embedthumbnails{page.Thumbnail.ID}.jpg")
    End Using
  Next
End Using
```

![](../../../images/pdf/embedthumbnails.pdf.png)
embedthumbnails.pdf - [Page 1]

