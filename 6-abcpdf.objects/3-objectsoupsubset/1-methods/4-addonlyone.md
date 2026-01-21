---
title: "4-addonlyone"
css: "abcpdf-docs.css"
---

|  |  | AddOnlyOne Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add just this object ignoring any objects it may refer to. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp bool AddOnlyOne(IndirectObject io) ``` [Visual Basic] ``` Function AddOnlyOne(io As IndirectObject) As Boolean ``` `may throw Exception()` |  |  | 
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
| io | The IndirectObject to be added. | 
| return | True if the item was added. | 

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
      
| Add a parent object ignoring any objects it may refer to. If the item was added this function returns true. If the item was not added because the subset already contained it or because the RemapTypes specified a different remapping then the function returns false. If the specified object is not part of the soup specified in the ObjectSoupSubset constructor then an exception will be raised. |  |  | 
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