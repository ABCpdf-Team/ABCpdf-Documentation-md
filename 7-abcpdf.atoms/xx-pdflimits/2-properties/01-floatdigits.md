---
title: "01-floatdigits"
css: "abcpdf-docs.css"
---

|  |  | FloatDigits Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Int32` | 5 | No | The number of digits that can be written in the fractional part of a floating point number. | 

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
      
| The number of digits that can be written in the fractional part of a floating point number. For example if the value was five then the smallest number which could be represented would be 0.00001. The PDF 1.4 specification limited this value to five digits. You might ask how relevant the PDF 1.4 spec is now - after all it came out in 2003 and then was superseded in 2004. However the PDF/A spec is designed against the PDF 1.4 spec so is is not just that the document might display badly in a version of Acrobat from fifteen years ago. This value defaults to five and may be set to any value between five and thirty-eight. |  |  | 
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