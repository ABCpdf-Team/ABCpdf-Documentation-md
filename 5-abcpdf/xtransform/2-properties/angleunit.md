# AngleUnit&nbsp;Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| [C#]`AngleUnitType`[Visual Basic]`AngleUnitType` | Degrees | No | The angle unit, degrees or radians. | 

## Notes

Specify the angle unit as used by the [Rotate](../1-methods/rotate.md) method.

The AngleUnitType enumeration may take the following values:

- Degrees
- Radians

## Example

[C#]

```csharp
using var doc = new Doc();
doc.FontSize = 96;
doc.TextStyle.HPos = 0.5;
doc.TextStyle.VPos = 0.5;
doc.Transform.Rotate(90, doc.Rect.Width / 2, doc.Rect.Height / 2);
doc.TextStyle.Underline = true;
doc.AddText("Hello World rotated by 90 degrees");
doc.Page = doc.AddPage();
doc.Transform.AngleUnit = WebSupergoo.ABCpdf13.XTransform.AngleUnitType.Radians;
doc.Transform.Rotate(-1 * Math.PI / 2, doc.Rect.Width / 2, doc.Rect.Height / 2);
doc.AddText("Hello World rotated back by PI/2 radians");
doc.Save(Server.MapPath("transformrotate.pdf"));
```

[Visual Basic]

```vbnet
Using doc As New Doc()
  doc.FontSize = 96
  doc.TextStyle.HPos = 0.5
  doc.TextStyle.VPos = 0.5
  doc.Transform.Rotate(90, doc.Rect.Width / 2, doc.Rect.Height / 2)
  doc.TextStyle.Underline = True
  doc.AddText("Hello World rotated by 90 degrees")
  doc.Page = doc.AddPage()
  doc.Transform.AngleUnit = WebSupergoo.ABCpdf13.XTransform.AngleUnitType.Radians
  doc.Transform.Rotate(-1 * Math.PI / 2, doc.Rect.Width / 2, doc.Rect.Height / 2)
  doc.AddText("Hello World rotated back by PI/2 radians")
  doc.Save(Server.MapPath("transformrotate.pdf"))
End Using
```

![](../../../images/pdf/transformrotate.pdf.png)transforrotate.pdf, page 1

![](../../../images/pdf/transformrotate.pdf2.png)transforrotate.pdf, page 2

</div>