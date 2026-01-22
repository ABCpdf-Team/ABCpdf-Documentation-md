# SetCmyk Function

Set the color to an CMYK value.

## Syntax

[C#]

```csharp
void SetCmyk(int cyan, int magenta, int yellow, int black)void SetCmyk(int cyan, int magenta, int yellow, int black, int alpha)void SetCmyk(double cyan, double magenta, double yellow, double black)void SetCmyk(double cyan, double magenta, double yellow, double black, double alpha)
```

[Visual Basic]

```vb
Sub SetCmyk(cyan As Integer, magenta As Integer, yellow As Integer, black As Integer)Sub SetCmyk(cyan As Integer, magenta As Integer, yellow As Integer, black As Integer, alpha as Integer)Sub SetCmyk(cyan As Double, magenta As Double, yellow As Double, black As Double)Sub SetCmyk(cyan As Double, magenta As Double, yellow As Double, black As Double, alpha as Double)
```

## Params

| **Name** | **Description** |
| --- | --- |
| cyan | The amount of cyan (0 to 100). |
| magenta | The amount of magenta (0 to 100). |
| yellow | The amount of yellow (0 to 100). |
| black | The amount of black (0 to 100). |
| alpha | The level of opacity from transparent through to fully opaque (0 to 255). |

## Notes

Set the color to CMYK and provide a value for it.

Optionally set the alpha value to specify a transparency level. If this parameter is omitted the color is set to fully opaque - no transparency.

## Example

Also see example code in: [Page GetBitmap Function](6-abcpdf.objects/page/1-methods/getbitmap.md).
