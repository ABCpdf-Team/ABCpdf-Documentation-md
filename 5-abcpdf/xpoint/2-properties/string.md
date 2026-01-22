# String Property

## Notes

Allows you to access to the point as a string.

The format of the string must be "x y".

## Example

The following code.

[C#] var pt = new XPoint(); pt.String = "20 10"; Response.Write($"X = {pt.X}"); Response.Write("<br>"); Response.Write($"Y = {pt.Y}"); [Visual Basic] Dim pt As New XPoint() pt.String = "20 10" Response.Write($"X = {pt.X}") Response.Write("<br>") Response.Write($"Y = {pt.Y}")

Produces the following output. X = 20 Y = 10

Also see example code in: ABCpdf Advanced Graphics Example, ABCpdf Fields, Markup and Movies Example, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XTransform Invert Function, XTransform Reset Function, XTransform Rotate Function.

