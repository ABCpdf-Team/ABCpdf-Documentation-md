---
title: "gamma"
css: "abcpdf-docs.css"
---

|  |  | Gamma Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp ArrayAtom ``` [Visual Basic] `ArrayAtom` | n/a | No | The gamma correction for the color space | 

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
      
| The gamma correction for the color space. This property is only valid for color spaces in which the ColorSpaceType is CallGray or CalRGB. Gamma is defined for each component of a calibrated color space. So for a CalGray color space it has one entry and for a CalRGB color space it has three. This means that for a CalGray color space this property will be a NumAtom and for a CalRGB color space it will be an ArrayAtom with three entries. Each gamma entry must be positive and is generally greater than or equal to one. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we show how to use the Gamma property with a calibrated grayscale color space. [C#] ```csharp using var doc = new Doc(); doc.Width = 80; doc.Rect.Inset(50, 50); var cs = new ColorSpace(doc.ObjectSoup, ColorSpaceType.CalGray); ((NumAtom)cs.Gamma).Real = 1.2; doc.ColorSpace = cs.ID; doc.Color.SetComponents(0.9); // gray doc.AddOval(true); doc.Save(Server.MapPath("examplecalgraycolorspace.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Width = 80 doc.Rect.Inset(50, 50) Dim cs As New ColorSpace(doc.ObjectSoup, ColorSpaceType.CalGray) DirectCast(cs.Gamma, NumAtom).Real = 1.2 doc.ColorSpace = cs.ID doc.Color.SetComponents(0.9) ' gray doc.AddOval(True) doc.Save(Server.MapPath("examplecalgraycolorspace.pdf")) End Using ``` examplecalgraycolorspace.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>