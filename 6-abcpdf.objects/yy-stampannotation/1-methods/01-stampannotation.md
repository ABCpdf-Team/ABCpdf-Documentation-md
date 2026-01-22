# StampAnnotation Function

Add stamp annotation to the current page of the doc.

## Syntax

[C#]

```csharp
<a href="../default.htm">StampAnnotation</a>(Doc doc, XRect rect, string caption, XColor color)
```

[Visual Basic]

```vb
<a href="../default.htm">StampAnnotation</a>(doc As Doc, rect As XRect, caption As string, color As XColor)
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | Doc |
| rect | Annotation rectangle |
| caption | The text of the stamp. |
| color | The color of the stamp. |

## Notes

Add stamp annotation to the current page of the doc.

The supplied caption will be rendered in Helvetica Bold Oblique. The width of the provided rect will be adjusted to reflect the aspect ratio of the caption text. If you wish to maintain the original rect you can assign it to the [Rect](annotation/2-properties/rect.md) property after construction of the Stamp.

## Example

None
