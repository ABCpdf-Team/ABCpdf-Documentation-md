---
title: "basecolorspacetype"
css: "abcpdf-docs.css"
---

|  |  | BaseColorSpaceType Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp ColorSpaceType ``` [Visual Basic] `ColorSpaceType` | n/a | Yes | The base type of color space. | 

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
      
| The base color space is relevant for cases in which the ColorSpaceType property is Indexed. An Indexed color space contains a palette of colors indexed by number. Each item in the palette is a color in a different color space. As such the Indexed color space has a base color space in which the palette colors are defined. This property allows you to determine the base color space for an Indexed color space. If the color space is not Indexed then this property is equal to the ColorSpaceType property. |  |  | 
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