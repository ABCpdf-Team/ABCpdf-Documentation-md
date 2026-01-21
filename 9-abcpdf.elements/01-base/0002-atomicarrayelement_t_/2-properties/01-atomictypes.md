---
title: "01-atomictypes"
css: "abcpdf-docs.css"
---

|  |  | AtomicTypes Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp AtomicTypes ``` [Visual Basic] `AtomicTypes` | null | No | The Type of elements within the Array. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The Type of elements within the Array. This indicates the types of Atom that are acceptable in this Array. For example an AtomicArray of strings may accept NameAtoms, or StringAtoms or indeed both. This is a flags based enum so more than one type may be indicated by combining values. The possible values are:. NoneNamesStringsNumbersBooleans. The AtomicTypes type is a flags type enumeration so different values can be combined together using bitwise operations. It may take the following values: |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>