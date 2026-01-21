---
title: "widths"
css: "abcpdf-docs.css"
---

|  |  | Widths Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [] [Visual Basic] `Integer()` | n/a | Yes | The widths of the characters in the font. | 

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
      
| The character widths for all the characters in the font. The array is indexable by Unicode value. For example to find the width of a space (ASCII 32) you would simply reference item 32 in the array. The values are measured in in 1000ths of a PDF unit. Characters with no representation in the font are assigned a width of -1. |  |  | 
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