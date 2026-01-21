---
title: "blackpoint"
css: "abcpdf-docs.css"
---

|  |  | BlackPoint Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XColor ``` [Visual Basic] `XColor` | n/a | No | The black point for the color space specified in CIE 1931 XYZ space | 

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
      
| The black point for the color space specified in CIE 1931 XYZ space. This property is only valid for color spaces in which the ColorSpaceType is CallGray, CalRGB or Lab. All components for this valud must be non-negative. The default for this peroperty is 0 0 0. When you set this property a clone of the XColor you assign is created to avoid one XColor being shared by multiple color spaces. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the WhitePoint property. Also see example code in: ColorSpace WhitePoint Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>