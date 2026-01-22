# Alpha Property

## Notes

Allows you to get or set the alpha opacity of the color.

Alpha values can range from 0 to 255. Zero indicates fully transparent and 255 indicates fully opaque.

## Example

Here we create a PDF document showing how different values of alpha result in different levels of transparency.

[C#] using var doc = new Doc(); doc.Rect.Inset(20, 20); doc.FontSize = 300; for (int i = 1; i <= 10; i++) { doc.Color.Alpha = 255 / i; doc.AddText(doc.Color.Alpha.ToString()); doc.Rect.Move(25, -50); } doc.Save(Server.MapPath("coloralpha.pdf")); [Visual Basic] Using doc As New Doc() doc.Rect.Inset(20, 20) doc.FontSize = 300 Dim i As Integer = 1 While i <= 10 doc.Color.Alpha = 255 / i doc.AddText(doc.Color.Alpha.ToString()) doc.Rect.Move(25, -50) System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While doc.Save(Server.MapPath("coloralpha.pdf")) End Using

coloralpha.pdf

Also see example code in: SwfImportOperation Import Function.

