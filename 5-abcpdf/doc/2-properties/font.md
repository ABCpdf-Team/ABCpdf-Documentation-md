# Font Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | No | The current Font ID. | 

## Notes

The font used for drawing text.

This property holds the current Font ID and determines the style of text that is added to the document using methods like [AddText](../1-methods/addtext.md).

To get a Font ID you need to add your font to the current document using the [AddFont](../1-methods/addfont.md) method.

The Font property is an accessor for the the[XTextStyle.Font](../../xtextstyle/2-properties/font.md) property.

## Example

The following example adds two blocks of styled text to a document. The first block is in Helvetica and the second in Courier.

[C#]

```csharp
using var doc = new Doc();
doc.FontSize = 96; // big text
doc.Font = doc.AddFont("Helvetica");
doc.AddText("Helvetica Text.");
doc.Font = doc.AddFont("Courier");
doc.AddText("Courier Text.");
doc.Save(Server.MapPath("docfont.pdf"));
```

**[Visual Basic]**

```vbnet
Using doc As New Doc()
  doc.FontSize = 96
  ' big text
  doc.Font = doc.AddFont("Helvetica")
  doc.AddText("Helvetica Text.")
  doc.Font = doc.AddFont("Courier")
  doc.AddText("Courier Text.")
  doc.Save(Server.MapPath("docfont.pdf"))
End Using
```

![](../../../images/pdf/docfont.pdf.png) docfont.pdf

Also see example code in: [ABCpdf Unicode Example](../../../4-examples/12-unicode.md), [ABCpdf eForm Placeholder Example](../../../4-examples/15-eform2.md), [ABCpdf eForm Stamp Example](../../../4-examples/15-eform3.md), [ABCpdf eForm FDF Example](../../../4-examples/16-eformfdf.md), [ABCpdf Fields, Markup and Movies Example](../../../4-examples/18-annotations.md), [Doc AddFont Function](../1-methods/addfont.md), [Doc AddText Function](../1-methods/addtext.md), [Doc EmbedFont Function](../1-methods/embedfont.md), [Doc String Property](string.md), [FontObject Widths Property](../../../6-abcpdf.objects/fontobject/2-properties/widths.md), [ArrayAtom FromContentStream Function](../../../7-abcpdf.atoms/arrayatom/1-methods/fromcontentstream.md).