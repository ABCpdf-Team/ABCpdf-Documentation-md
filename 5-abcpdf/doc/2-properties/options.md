# Options Property

## Notes

The options property is an advanced feature which allows low level control over PDF drawing. It is important to use it correctly as incorrect use can corrupt your documents.

The value of the options property is inserted into the PDF content stream after state has been established but before any drawing has taken place. You can use this property to insert your own state commands. This is most commonly used for drawing dashed lines.

FillRect, FrameRect, AddLine and AddArc all insert the options parameter.

You can find details of graphics state parameters and how to use them in the Adobe PDF Specification.

## Example

The following code adds an arc to a document. It uses the options parameter to make the line dashed rather than solid.

[C#] using var doc = new Doc(); doc.Width = 24; doc.Color.String = "0 120 0"; doc.Options = "[6 10] 6 d"; doc.AddArc(0, 270, 300, 400, 200, 300); doc.Save(Server.MapPath("docoptions.pdf")); [Visual Basic] Using doc As New Doc() doc.Width = 24 doc.Color.String = "0 120 0" doc.Options = "[6 10] 6 d" doc.AddArc(0, 270, 300, 400, 200, 300) doc.Save(Server.MapPath("docoptions.pdf")) End Using

docoptions.pdf

