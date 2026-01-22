# Underline Property

## Notes

This property determines whether underlining is applied to text.

## Example

In this example we add some underlined text to a document.

[C#] using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur."; doc.Rect.Inset(20, 40); doc.TextStyle.Size = 96; doc.TextStyle.Underline = true; doc.AddText(text); doc.Save(Server.MapPath("styleunderline.pdf")); [Visual Basic] Using doc As New Doc() Dim theText As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur." doc.Rect.Inset(20, 40) doc.TextStyle.Size = 96 doc.TextStyle.Underline = True doc.AddText(theText) doc.Save(Server.MapPath("styleunderline.pdf")) End Using

styleunderline.pdf

Also see example code in: XTransform AngleUnit�Property.

