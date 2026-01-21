---
title: "removeitem"
css: "abcpdf-docs.css"
---

|  |  | RemoveItem Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Removes the named entry from the Atom if it is a DictAtom. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp static void RemoveItem(Atom atom, string key) ``` [Visual Basic] `Shared Sub RemoveItem(atom As Atom, key As String)` |  |  | 
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
| atom | The Atom from which the item should be removed. | 
| key | The name of the item to be removed. | 

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
      
| DictAtoms can contain other Atoms referenced by name. This function allows you to remove a named item from a DictAtom. If the atom supplied is not a DictAtom then calling this function will have no effect. |  |  | 
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