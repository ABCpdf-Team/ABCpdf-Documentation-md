# Recolor Function

Recolor pages in a document.

## Syntax

[C#]

```csharp
void Recolor(Doc doc)void Recolor(Pages pages)void Recolor(Page page)
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | The document to be recolored. |
| pages | The pages to be recolored as referenced by a Pages IndirectObject. |
| page | The page to be recolored as referenced by a Page IndirectObject. |

## Notes

Converts the specified pages from one color space to another.

The destination color space is specified by assigning a value to the [DestinationColorSpace](2-properties/destinationcolorspace.md) property. All images used on the page are converted to the new color space. All color operators used in the page content stream are converted to the new color space.

Annotations and fields are not part of the page but instead float over the page. You can choose whether to convert the appearance stream of any annotations or leave them in their native color space. This is controlled using the [ConvertAnnotations](2-properties/convertannotations.md) property.

Colors can only be sensibly mapped from one color space to another if we know something about the characteristics of the color space. If your color spaces do not contain this information (e.g. if they are device color spaces) then ABCpdf will use a default color profile.

An exception will be thrown if the operation is not possible. This may happen if the IndirectObjects provided are not in an ObjectSoup or if the destination ColorSpace is in some way invalid.

As part of the Recolor process, all images used on the page(s) are also recolored. (See also [PixMap.Recolor](6-abcpdf.objects/pixmap/1-methods/recolor.md).) After the recolor process has been completed these [PixMap](6-abcpdf.objects/pixmap/default.md) objects will no longer be compressed. You may wish to analyse and recompress these images by pre and post processing them during the [ProcessingObject](1-operation/3-events/1-processingobject.md) and [ProcessedObject](1-operation/3-events/2-processedobject.md) events.

---
---

## Example

Here we recolor one page out of a document. We pick up the [ProcessingObject](1-operation/3-events/1-processingobject.md) events so that we can store the source color space for all the PixMap objects which are processed. We do not want to convert CMYK pixmaps so we set the Cancel property to true if we find these. We then pick up the [ProcessedObject](1-operation/3-events/2-processedobject.md) events so that we can recompress the PixMap objects after they have been recolored. We vary the recompression method used dependent on the source color space and the size of the image. Here we use standard delegates for backwards compatibility with older code. However anonymous delegates will provide a more compact solution.

[C#]

```csharp
using var doc = new Doc();
doc.Read("../mypics/sample.pdf");
MyOp.Recolor(doc, (Page)doc.ObjectSoup[doc.Page]);
doc.Save("RecolorOperation.pdf");
```

Also see example code in: [RecolorOperation IccCmyk Property](2-properties/icccmyk.md).
