# SetFont Function

Sets the font and font size to be used for text

## Syntax

[C#]

```csharp
vitual void SetFont(<a href="../../fontobject/default.htm">FontObject</a> font, double size)
```

[Visual Basic]

```vb
Sub SetFont(font As <a href="../../fontobject/default.htm">FontObject</a>, size As Double)
```

## Params

| **Name** | **Description** |
| --- | --- |
| font | The font to be assigned to the field. |
| size | The font size to be assigned to the field. |

## Notes

Sets the font and font size to be used for text.

This function works by changing the [DefaultAppearance](2-properties/defaultappearance.md) for the field using the specified [FontObject](fontobject/default.md) and size.

Properties such ase the [TextFont](2-properties/textfont.md) and [TextSize](2-properties/textsize.md) get the effective value which may be inherited. Calling this funtion sets the value on this item itself which will override any inherited value.

Passing a font value of null will remove both the font and size from the item itself though a value may be still be present if it is inherited from a parent field or from document defaults.

A zero size font indicates that the font should scale so that it fits the size of the field. Negative font heights appear the same as positive ones but are best avoided as they are likely to cause confusion.

The appearance of the field is not updated until you change the [Value](2-properties/value.md) or call [UpdateAppearance](1-methods/updateappearance.md).

## Example

None
