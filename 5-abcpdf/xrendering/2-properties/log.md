---
title: "log"
css: "abcpdf-docs.css"
---

|  |  | Log Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "" | Yes | The log for the last render. | 

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
      
| During rendering inconsistencies may be detected in the PDF or in the environment. For example if a PDF contains a corrupt image then it may not be possible to display it. If a PDF contains a reference to a font which is not on the current system then a font substitution may be required. ABCpdf will do its best to complete the render even if errors or inconsistencies are found. However it will log these type of issues and make the log available via this property. This can be useful for debugging purposes. |  |  | 
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