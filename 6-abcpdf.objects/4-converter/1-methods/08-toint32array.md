---
title: "08-toint32array"
css: "abcpdf-docs.css"
---

|  |  | ToInt32Array Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Attempts to convert an ArrayAtom into an array of ints, resolving any references as necessary. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual int[] ToInt32Array(Atom atom, int def) ``` [Visual Basic] ``` Overridable Function ToInt32Array(atom As Atom, def As int) As Integer[] ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The ArrayAtom from which to obtain the values. | 
| def | A default value for any entries which could not be converted to the correct type. | 
| return | The array. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Attempts to convert an ArrayAtom into an array of ints, resolving any references as necessary. If the atom does not resolve to an ArrayAtom, then the return value will be null. |  |  | 
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