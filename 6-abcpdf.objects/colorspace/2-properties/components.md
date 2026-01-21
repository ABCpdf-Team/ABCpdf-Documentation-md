---
title: "components"
css: "abcpdf-docs.css"
---

|  |  | Components Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | n/a | Yes | The number of color components in the color space. | 

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
      
| Different color spaces have different numbers of components. For example RGB color spaces have three components and CMYK color spaces have four. This property allows you to determine the number of color components in the color space. Indexed color spaces define colors via a palette. So although a color value is determined via a single index into a palette, the number of components is determined by the number of color components in the palette. For example the number of components in an indexed RGB color space is three. Pattern color spaces are special and have no components. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>