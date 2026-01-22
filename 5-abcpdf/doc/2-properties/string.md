# String Property

## Notes

A string representation of the graphic style of the document.

This covers the Transform, ColorSpace, Color, Font, TextStyle, Width and Options properties. However it does not cover the Page, Layer, Rect or Pos properties.

## Example

In this example we show how to use the String property to implement a graphics state stack with Push and Pop operators.

[C#] using var doc = new Doc(); doc.FontSize = 64; doc.Rect.Inset(20, 20); doc.Font = doc.AddFont("Helvetica"); var state = new Stack<string>(); state.Push(doc.String); doc.AddText("Black Helvetica\r\n\r\n"); doc.Color.SetRgb(255, 0, 0); doc.Font = doc.AddFont("Helvetica-Oblique"); doc.AddText("Red Helvetica-Oblique\r\n\r\n"); doc.String = state.Pop(); doc.AddText("Black Helvetica again\r\n\r\n"); doc.Save(Server.MapPath("savestate.pdf")); [Visual Basic] Using doc As New Doc() doc.FontSize = 64 doc.Rect.Inset(20, 20) doc.Font = doc.AddFont("Helvetica") Dim state As New Stack(Of String)() state.Push(doc.String) doc.AddText("Black Helvetica" & vbCr & vbLf & vbCr & vbLf) doc.Color.SetRgb(255, 0, 0) doc.Font = doc.AddFont("Helvetica-Oblique") doc.AddText("Red Helvetica-Oblique" & vbCr & vbLf & vbCr & vbLf) doc.String = state.Pop() doc.AddText("Black Helvetica again" & vbCr & vbLf & vbCr & vbLf) doc.Save(Server.MapPath("savestate.pdf")) End Using

savestate.pdf

