---
title: "09-todoublearray"
css: "abcpdf-docs.css"
---

|  |  | ToDoubleArray Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Attempts to convert an ArrayAtom into an array of doubles, resolving any references as necessary. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual double[] ToDoubleArray(Atom atom, double def) ``` [Visual Basic] ``` Overridable Function ToDoubleArray(atom As Atom, def As double) As Double[] ``` |  |  | 
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
      
| Attempts to convert an ArrayAtom into an array of doubles, resolving any references as necessary. If the atom does not resolve to an ArrayAtom, then the return value will be null. |  |  | 
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