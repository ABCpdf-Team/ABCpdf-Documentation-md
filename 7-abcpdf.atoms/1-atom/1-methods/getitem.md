---
title: "getitem"
css: "abcpdf-docs.css"
---

|  |  | GetItem Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the specified item from the Atom if it is of a type which contains other Atoms. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static Atom GetItem(Atom atom, string key) static Atom GetItem(Atom atom, int index) ``` [Visual Basic] ``` Shared Function GetItem(atom As Atom, key As String) As Atom Shared Function GetItem(atom As Atom, index As Integer) As Atom ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The Atom to get the item from. | 
| key | The name of the item to be retrieved. | 
| index | The index of the item to be retrieved. | 
| return | The returned Atom. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Both DictAtoms and ArrayAtoms can contain other Atoms. This function allows you to get an item from an ArrayAtom or DictAtom. Entries in ArrayAtoms can be referenced by number. If the supplied atom is not an ArrayAtom or if it is null or if the index is outside the bounds of the array then null will be returned. Entries in DictAtoms can be referenced by name or by number. If the supplied atom is not a DictAtom or if it is null or if the name is not a key in the dictionary or if the index is outside the bounds of the dictionary then null will be returned. |  |  | 
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