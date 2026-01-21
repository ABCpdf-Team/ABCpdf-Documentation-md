---
title: "setitem"
css: "abcpdf-docs.css"
---

|  |  | SetItem Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a specified item to the Atom if it is of a type which contains other Atoms. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static Atom SetItem(Atom atom, string key, Atom val) static Atom SetItem(Atom atom, int index, Atom val) ``` [Visual Basic] ``` Shared Function SetItem(atom As Atom, key As String, val As Atom) As Atom Shared Function SetItem(atom As Atom, index As Integer, val As Atom) As Atom ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The Atom to which the item should be added. | 
| key | The name of the item to be added. | 
| index | The index at which the item should be added. | 
| return | The returned Atom. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Both DictAtoms and ArrayAtoms can contain other Atoms. This function allows you to add an item to an ArrayAtom or DictAtom. If the container Atom supplied is not a DictAtom or an ArrayAtom then insertion will not be successful. Entries in ArrayAtoms can be referenced by number. If the container Atom supplied is an ArrayAtom and the index supplied is within the bounds of the array then insertion will be successful. If the index supplied is less than zero then the value Atom will be added to the end of the array. Again insertion will be successful. Entries in DictAtoms can be referenced by name. If the container Atom supplied is a DictAtom and the key supplied is not empty then insertion will be successful. If insertion was successful the function will return the Atom which was added. If it was not successful it will return null. |  |  | 
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