---
title: "12-toint32dictionary"
css: "abcpdf-docs.css"
---

|  |  | ToInt32Dictionary Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Attempts to convert a DictAtom into a Dictionary of ints, resolving any references as necessary. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual Dictionary ToInt32Dictionary(Atom atom, int def) ``` [Visual Basic] ``` Overridable Function ToInt32Dictionary(atom As Atom, def As int) As Dictionary ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The DictAtom from which to obtain the values. | 
| def | A default value for any entries which could not be converted to the correct type. | 
| return | The dictionary. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Attempts to convert a DictAtom into a Dictionary of ints, resolving any references as necessary. If the atom does not resolve to an DictAtom, then the return value will be null. |  |  | 
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