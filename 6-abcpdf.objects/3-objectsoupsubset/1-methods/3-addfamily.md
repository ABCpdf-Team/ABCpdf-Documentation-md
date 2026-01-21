---
title: "3-addfamily"
css: "abcpdf-docs.css"
---

|  |  | AddFamily Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add a parent object along with all objects it refers to. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp int AddFamily(IndirectObject parent) int AddFamily(DictAtom dict) ``` [Visual Basic] ``` Function AddFamily(parent As IndirectObject) As Integer Function AddFamily(dict As DictAtom) As Integer ``` `may throw Exception()` |  |  | 
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
| parent | The IndirectObject to be added. | 
| dict | A dictionary atom to be added. | 
| return | The number of objects that were added. | 

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
      
| Add a parent object along with all objects it refers to. If a dictionary is specified there is no parent. In this situation only the objects referred to in the dictionary will be added. If the parent or dictionary is not part of the soup specified in the ObjectSoupSubset constructor then an exception will be raised. |  |  | 
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