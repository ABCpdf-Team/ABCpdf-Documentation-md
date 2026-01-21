---
title: "setstream"
css: "abcpdf-docs.css"
---

# SetStream Function

Load an image from stream.

## Syntax

**[C#]**

```csharp
void SetStream(Stream stream)
```

<span class=language>[Visual
            Basic]</span>  
`Sub SetStream(stream As Stream)``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| Stream | The stream containing the graphic. | 

## Notes

Load an image from stream.

The stream can contain any of the following types: JPEG, GIF, TIFF, BMP, PNG, PSD, PDB, EXIF, WMF, EMF, EPS, PS or SWF (Flash).

Ultimately each import goes through a [ReadModule](../../xreadoptions/2-properties/1-readmodule.md) so for details of additional formats supported and the way they are imported, see the [ReadModule](../../xreadoptions/2-properties/1-readmodule.md) property.

Different images within the file can be accessed using the [Frame](../2-properties/frame.md) property. Different portions of the image can be selected using the [Selection](../2-properties/selection.md) property.

## Example

Here we read a TIFF file and present the data to the XImage object. We then add the image to our document and then save the PDF.

[C#]

```csharp
using var img = new XImage();
string path = Server.MapPath("../mypics/mypic.jpg");
using var stream = File.OpenRead(path);
img.SetStream(stream);
using var doc = new Doc();
doc.Rect.Inset(20, 20);
doc.AddImageObject(img, false);
doc.Save(Server.MapPath("imagesetstream.pdf"));
```

<span class=language>[Visual
            Basic]</span>
```vbnet
Dim theImg As New XImage()
Dim thePath As String
thePath = Server.MapPath("../mypics/mypic.jpg")
Dim theStream As Stream
theStream = File.OpenRead(thePath)
theImg.SetStream(theStream)
theStream.Close()
Dim doc As New Doc()
doc.Rect.Inset(20, 20)
doc.AddImageObject(theImg, False)
theImg.Clear()
doc.Save(Server.MapPath("imagesetstream.pdf"))
doc.Clear()
```

![](../../../images/pdf/imagesetfile.pdf.png)imagesetstream.pdf