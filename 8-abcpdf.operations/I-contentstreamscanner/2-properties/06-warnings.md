---
title: "06-warnings"
css: "abcpdf-docs.css"
---

|  |  | Warnings Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp List ``` [Visual Basic] `List` | null | No | Content streams contain operators and parameters. | 

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
      
| Content streams contain operators and parameters. If part of the the content stream is badly formed - for example if a parameter is missing - then an internal exception will be raised. Typically you want to move on past this and try and recover. Just because a text spacing operator is incorrect does not mean you want to abandon the whole page. Equally you do not want to completely ignore this type of error. As such, if you assign a value to this proprty, any errors or warnings will be stored here. |  |  | 
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