---
title: "rotate"
css: "abcpdf-docs.css"
---

# Rotate Function

Rotates the page by a multiple of ninety degrees.

## Syntax

**[C#]**

```csharp
void Rotate(int angle)
```

<span class=language>[Visual
            Basic]</span>  

            `Sub Rotate(angle As Integer)``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| angle | The number of degrees clockwise by which to rotate the page. | 

## Notes

Rotates the page by a multiple of ninety degrees.

By providing the Rotation property to this function you can derotate a page. The [Rotation](../2-properties/rotation.md) property and page bounding boxes ([MediaBox](../2-properties/mediabox.md), [CropBox](../2-properties/cropbox.md), [BleedBox](../2-properties/bleedbox.md), [TrimBox](../2-properties/trimbox.md) and [ArtBox](../2-properties/artbox.md)) will be adjusted to reflect the new viewing orientation.

If a value is provided which is not a multiple of ninety degrees, an exception will be raised.

## Example

None.