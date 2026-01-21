---
title: "7-insert"
css: "abcpdf-docs.css"
---

|  |  | Insert Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Inserts an Atom into the array at the specified position. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void Insert(int index, Atom value) ``` [Visual Basic] `Sub Insert(index As Integer, value As Atom)` `may throw ArgumentOutOfRangeException()` |  |  | 
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
| value | The Atom to insert into the array. | 

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
      
| Inserts an Atom into the array at the specified position. If the index equals the number of items in the array then the Atom is appended to the end. Atoms can exist in only one place at a time. If the Atom supplied is already contained by another object then a Clone of the Atom is added. Adding a null value will result in a NullAtom being added to the array. If the index is not a valid index this method throws an ArgumentOutOfRangeException. |  |  | 
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