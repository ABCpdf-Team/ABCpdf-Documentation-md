---
title: "colorspace"
css: "abcpdf-docs.css"
---

|  |  | ColorSpace Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Construct a ColorSpace. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp ColorSpace(ObjectSoup soup) ColorSpace(ObjectSoup soup, ColorSpaceType space) ``` [Visual Basic] ``` Sub New(soup As ObjectSoup) Sub New(soup As ObjectSoup, space As ColorSpaceType) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created StreamObject. | 
| space | The type of color space required. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Create a ColorSpace. If a color space is not specified the default of DeviceRGB will be used. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the PixMap.Recolor function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>