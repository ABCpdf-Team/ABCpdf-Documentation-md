---
title: "setmask"
css: "abcpdf-docs.css"
---

# SetMask Function

Assign a soft mask to the image.

## Syntax

**[C#]**

```csharp
void SetMask(XImage mask, bool invert)
```

<span class=language>[Visual Basic]</span>  
`Sub SetMask(mask As XImage, invert As Boolean)``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| mask | The image containing the soft mask. | 
| invert | Whether to invert the mask. | 

## Notes

Assign a soft mask or alpha channel. Soft masks are used to assign levels of transparency to an image.

The mask provided will be converted to a grayscale intensity map and may be scaled to ensure that the dimensions of the mask match those of the image. The assigned mask applies to all frames of the current image.

If the Invert parameter is set then the mask will be inverted - making transparent areas opaque and opaque areas transparent.

Different images within the mask can be accessed using the [Frame](../2-properties/frame.md) property. Different portions of the mask can be selected using the [Selection](../2-properties/selection.md) property.

Note that transparency is only applied to an Image if the [Indirect](../2-properties/indirect.md) property is true (which is generally the case).

## Example

Here we read a TIFF file and present the data to the Image object. We then read a mask image and assign that to our Image. Finally we add the image to our document and then save the PDF.

[C#]

```csharp
using var doc = new Doc();
using var img = new XImage();
using var msk = new XImage();
img.SetFile(Server.MapPath("../mypics/mypic.jpg"));
msk.SetFile(Server.MapPath("../mypics/mymask.jpg"));
img.SetMask(msk, true);
doc.Color.String = "0 0 0";
doc.FillRect();
doc.Rect.Inset(20, 20);
doc.AddImageObject(img, true);
doc.Save(Server.MapPath("imagesetmask.pdf"));
```

<span class=language>[Visual
            Basic]</span>
```vbnet
Using doc As New Doc()
  Dim theImg As New XImage()
  Dim theMsk As New XImage()
  theImg.SetFile(Server.MapPath("../mypics/mypic.jpg"))
  theMsk.SetFile(Server.MapPath("../mypics/mymask.jpg"))
  theImg.SetMask(theMsk, True)
  theMsk.Clear()
  doc.Color.String = "0 0 0"
  doc.FillRect()
  doc.Rect.Inset(20, 20)
  doc.AddImageObject(theImg, True)
  theImg.Clear()
  doc.Save(Server.MapPath("imagesetmask.pdf"))
End Using
```

Given the following input images.

![](../../../images/pdf/image.pdf.png)mypic.jpg![](../../../images/pdf/mask.jpg)mymask.jpgThis is the kind of output you might expect.

![](../../../images/pdf/imagesetmask.pdf.png)imagesetmask.pdf