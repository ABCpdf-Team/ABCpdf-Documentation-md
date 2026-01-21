---
title: "formatfields"
css: "abcpdf-docs.css"
---

|  |  | FormatFields Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether values should be formatted before insertion into fields. | 

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
      
| This determines if values should be formatted before insertion. Acrobat uses JavaScript to implement number and date formats. Although this is something which is part of Acrobat rather than of the PDF specification you can ask ABCpdf to adhere to these formatting scripts. When this property is set to true ABCpdf will detect these standard scripts and generate appearances conforming with them. See the Field.Format property for details. It is unlikely you will want to change the value of this property. |  |  | 
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