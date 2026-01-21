---
title: "5-fromatom"
css: "abcpdf-docs.css"
---

|  |  | FromAtom Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create an XRect from a standard PDF Rectangle ArrayAtom. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static XRect FromAtom(IndirectObject io, ArrayAtom array) ``` [Visual Basic] ``` Shared Function FromAtom(io As IndirectObject, array As ArrayAtom) As XRect ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| io | Any IndirectObject from the document. | 
| array | An ArrayAtom containing four NumAtoms. | 
| return | The newly created XRect object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create an XRect from a standard PDF Rectangle ArrayAtom. Such arrays typically contain four numbers - lower left x and y coordinates followed by upper right x and y. However this is a convention and any two diagonally opposite points are acceptable. If the array is null or the entries do not resolve to four NumAtoms then the return value will be null. |  |  | 
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