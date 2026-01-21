---
title: "transform"
css: "abcpdf-docs.css"
---

# Transform Function

Transform the page contents and page bounding boxes.

## Syntax

**[C#]**

```csharp
void Transform(XTransform transform)
```

<span class=language>[Visual
            Basic]</span>  

            `Sub Transform(transform As XTransform)`
## Params

| Name | Description | 
| --- | --- |
| transform | The transform to apply. | 

## Notes

Transform the page contents and page bounding boxes ([MediaBox](../2-properties/mediabox.md), [CropBox](../2-properties/cropbox.md), [BleedBox](../2-properties/bleedbox.md), [TrimBox](../2-properties/trimbox.md) and [ArtBox](../2-properties/artbox.md)).

You can use this function to scale or otherwise alter a page.

## Example

None.