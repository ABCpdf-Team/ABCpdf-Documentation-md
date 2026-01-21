---
title: "3-add"
css: "abcpdf-docs.css"
---

|  |  | Add Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds an object to the Soup. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp int Add(IndirectObject value) ``` [Visual Basic] ``` Function Add(value As IndirectObject) As Integer ``` |  |  | 
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
| value | The IndirectObject to be added. | 
| return | The position in which the new element was inserted. | 

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
      
| This method adds an IndirectObject to the Soup. An IndirectObject can exist in only one ObjectSoup at a time. If the object supplied is already contained in another ObjectSoup then a Clone of the object is inserted. When an IndirectObject is inserted the ID is updated to reflect the position of the object within the Soup. |  |  | 
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