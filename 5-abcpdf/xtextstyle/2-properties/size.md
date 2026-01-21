# Size Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 10.0 | No | The current text size. | 

## Notes

This property determines the size of text that is added to the document using the [AddText](../../doc/1-methods/addtext.md) and [AddTextStyled](/5-abcpdf/doc/1-methods/addtextstyled.md) methods.

The Size property is equivalent to the the [Doc.FontSize](../../doc/2-properties/fontsize.md) property but unlike the FontSize property it allows fractional point sizes to be specified.

The font size is measured in units.

## Example

The following example adds two blocks of styled text to a document. The first block is in 96.5 point type and the second is in 192.5 point type.

[C#]

```csharp
using var doc = new Doc();
doc.TextStyle.Size = 96.5;
doc.AddText("Small ");
doc.TextStyle.Size = 192.5;
doc.AddText("Big");
doc.Save(Server.MapPath("stylesize.pdf"));
```

**[Visual Basic]**

```vbnet
Using doc As New Doc()
  doc.TextStyle.Size = 96.5
  doc.AddText("Small ")
  doc.TextStyle.Size = 192.5
  doc.AddText("Big")
  doc.Save(Server.MapPath("stylesize.pdf"))
End Using
```

![](../../../images/pdf/stylesize.pdf.png) stylesize.pdf

Also see example code in: [Doc TextStyle Property](../../doc/2-properties/textstyle.md), [XTextStyle Bold Property](bold.md), [XTextStyle CharSpacing Property](charspacing.md), [XTextStyle Indent Property](indent.md), [XTextStyle Italic Property](italic.md), [XTextStyle Justification Property](justification.md), [XTextStyle Kerning Property](kerning.md), [XTextStyle LeftMargin Property](leftmargin.md), [XTextStyle LineSpacing Property](linespacing.md), [XTextStyle Outline Property](outline.md), [XTextStyle ParaSpacing Property](paraspacing.md), [XTextStyle Strike Property](strike.md), [XTextStyle Strike2 Property](strike2.md), [XTextStyle Underline Property](underline.md), [XTextStyle WordSpacing Property](wordspacing.md), [Page GetBitmap Function](../../../6-abcpdf.objects/page/1-methods/getbitmap.md).