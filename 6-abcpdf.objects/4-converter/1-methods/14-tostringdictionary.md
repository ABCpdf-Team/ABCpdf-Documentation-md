---
title: "14-tostringdictionary"
css: "abcpdf-docs.css"
---

|  |  | ToStringDictionary Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Attempts to convert a DictAtom into a Dictionary of strings, resolving any references as necessary. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual Dictionary ToStringDictionary(Atom atom) ``` [Visual Basic] ``` Overridable Function ToStringDictionary(atom As Atom) As Dictionary ``` |  |  | 
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
| return | The dictionary. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Attempts to convert a DictAtom into a Dictionary of strings, resolving any references as necessary. If the atom does not resolve to an DictAtom, then the return value will be null. Any entries which could not be coverted to the correct type will be null. |  |  | 
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