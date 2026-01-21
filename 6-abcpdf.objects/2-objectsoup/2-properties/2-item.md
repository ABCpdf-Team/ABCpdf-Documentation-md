---
title: "2-item"
css: "abcpdf-docs.css"
---

|  |  | Item Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp IndirectObject this[int index] ``` [Visual Basic] `Default Property Item(index As Integer) As IndirectObject` | n/a | No | Gets or sets the object at the specified index. | 

`may throw ArgumentOutOfRangeException()`

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
      
| Gets or sets the IndirectObject at the specified index. In C# this property is the indexer for the class. An IndirectObject can exist in only one ObjectSoup at a time. If the object supplied is already contained in another ObjectSoup then a Clone of the object is inserted. When an IndirectObject is inserted the ID is updated to reflect the position of the object within the Soup. |  |  | 
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