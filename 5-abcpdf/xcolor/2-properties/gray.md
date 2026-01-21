---
title: "gray"
css: "abcpdf-docs.css"
---

|  |  | Gray Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | No | The gray component. | 

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
      
| Allows you to get or set the gray level. Grayscale levels can range from 0 (black) to 255 (white). Querying this property does not change the ColorSpace. This means you can obtain approximate Grayscale values for RGB or CMYK colors. However if you change the value of this property the color will automatically be converted to Grayscale. This property can also be used to specify levels for spot colorants. Levels can range from 0 (0% intensity) to 255 (100% intensity). See the AddColorSpaceSpot method for an example. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: Doc AddColorSpaceSpot Function, SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>