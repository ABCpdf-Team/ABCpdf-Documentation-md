---
title: "whitepoint"
css: "abcpdf-docs.css"
---

|  |  | WhitePoint Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XColor ``` [Visual Basic] `XColor` | n/a | No | The white point for the color space specified in CIE 1931 XYZ space | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The white point for the color space specified in CIE 1931 XYZ space. This property is only valid for color spaces in which the ColorSpaceType is CallGray, CalRGB or Lab. X and Y must be positive and Z must be one. The default for this peroperty is 0 0 0. When you set this property a clone of the XColor you assign is created to avoid one XColor being shared by multiple color spaces. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we show how to use the WhitePoint and BlackPoint with a calibrated RGB color space. [C#] ```csharp using var doc = new Doc(); doc.Width = 80; doc.Rect.Inset(50, 50); var cs = new ColorSpace(doc.ObjectSoup, ColorSpaceType.CalRGB); cs.WhitePoint.SetComponents(0.9, 1.0, 1.1); cs.BlackPoint = XColor.FromComponents(0.1, 0.1, 0.1); doc.ColorSpace = cs.ID; doc.Color.SetComponents(0.9, 0.1, 0.1); // red doc.AddOval(true); doc.Save(Server.MapPath("examplecalrgbcolorspace.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Width = 80 doc.Rect.Inset(50, 50) Dim cs As New ColorSpace(doc.ObjectSoup, ColorSpaceType.CalRGB) cs.WhitePoint.SetComponents(0.9, 1.0, 1.1) cs.BlackPoint = XColor.FromComponents(0.1, 0.1, 0.1) doc.ColorSpace = cs.ID doc.Color.SetComponents(0.9, 0.1, 0.1) ' red doc.AddOval(True) doc.Save(Server.MapPath("examplecalrgbcolorspace.pdf")) End Using ``` examplecalrgbcolorspace.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>