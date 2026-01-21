---
title: "7-insert"
css: "abcpdf-docs.css"
---

|  |  | Insert Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Inserts an object into the Soup at the specified position. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void Insert(int index, IndirectObject value) ``` [Visual Basic] ``` Sub Insert(index As Integer, value As IndirectObject) ``` `may throw NotSupportedException()` |  |  | 
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
| index | The zero-based index at which value should be inserted. | 
| return | The Object to insert into the Soup. | 

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
      
| Objects within a collection refer to each other by index. This means that once an object is inserted into the Soup it must stay at the same index. If it moves then references may be broken. Insertion at a particular position might require other objects to be moved. For this reason this method always throws a NotSupportedException. |  |  | 
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