---
title: "8-resolveref"
css: "abcpdf-docs.css"
---

|  |  | ResolveRef Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Resolves any indirect references and returns the final RefAtom. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp RefAtom ResolveRef(Atom atom) ``` [Visual Basic] ``` Function ResolveRef(atom As Atom) As RefAtom ``` |  |  | 
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
| atom | The Atom to resolve. | 
| return | The final RefAtom or null if no valid RefAtom could be found. | 

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
      
| Atoms come in two basic types. Data atoms like NumAtoms and NameAtoms contain actual data. RefAtoms contain a reference to an IndirectObject which contains another Atom. Quite often you will want to resolve any RefAtoms and just obtain the RefAtom pointing to the final IndirectObject - you want a pointer to the final item of data rather than a reference somewhere up the chain. This function takes an Atom. If it is a RefAtom it finds the IndirectObject to which it points. It keeps doing this until it finds the final IndirectObject in the chain. It returns the RefAtom which points to this IndirectObject. This method may return null if null is passed in, if the supplied Atom is not a RefAtom, if a RefAtom cannot be resolved or if a circular dependency is detected. The reason this function is a member of the IndirectObject is because resolving RefAtoms requires access to the ObjectSoup. The ObjectSoup is taken from the IndirectObject. |  |  | 
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