---
title: "7-resolve"
css: "abcpdf-docs.css"
---

|  |  | Resolve Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Resolves any indirect references and returns the Atom. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp Atom Resolve(Atom atom) ``` [Visual Basic] ``` Function Resolve(atom As Atom) As Atom ``` |  |  | 
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
| return | The final Atom or null if no Atom could be found. | 

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
      
| Atoms come in two basic types. Data atoms like NumAtoms and NameAtoms contain actual data. RefAtoms contain a reference to an IndirectObject which contains another Atom. Quite often you will want to resolve any RefAtoms and just obtain the Atom within the final IndirectObject - you want the final item of data rather than a reference to a piece of data. This function takes an Atom. If it is a RefAtom it finds the Atom to which it points. It keeps doing this until it finds and returns the final data Atom in the chain. This method may return null if null is passed in, if a RefAtom cannot be resolved or if a circular dependency is detected. The reason this function is a member of the IndirectObject is because resolving RefAtoms requires access to the ObjectSoup. The ObjectSoup is taken from the IndirectObject. |  |  | 
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