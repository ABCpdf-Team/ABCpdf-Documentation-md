---
title: "10-resolveobj"
css: "abcpdf-docs.css"
---

|  |  | ResolveObj Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Resolves any indirect references and returns the final IndirectObject. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IndirectObject ResolveObj(Atom atom) ``` [Visual Basic] ``` Function ResolveObj(atom As Atom) As IndirectObject ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The Atom to resolve. | 
| return | The final IndirectObject or null if no valid object could be found. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Atoms come in two basic types. Data atoms like NumAtoms and NameAtoms contain actual data. RefAtoms contain a reference to an IndirectObject which contains another Atom. Quite often you will want to resolve any RefAtoms and just obtain the final IndirectObject - you want a pointer to the final item of data rather than a reference somewhere up the chain. This function takes an Atom. If it is a RefAtom it finds the IndirectObject to which it points. It keeps doing this until it finds the final IndirectObject in the chain. It returns this IndirectObject. This method may return null if null is passed in, if the supplied Atom is not a RefAtom, if a RefAtom cannot be resolved or if a circular dependency is detected. The reason this function is a member of the IndirectObject is because resolving RefAtoms requires access to the ObjectSoup. The ObjectSoup is taken from the IndirectObject. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>