---
title: "1-fromlbwh"
css: "abcpdf-docs.css"
---

|  |  | FromLbwh Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Creates an XRect from a bottom left corner, a width and a height. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static XRect FromLbwh(double left, double bottom, double width, double height) ``` [Visual Basic] ``` Shared Function FromLbwh(left As Double, bottom As Double, width As Double, height As Double) As XRect ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| left | The left coordinate. | 
| bottom | The bottom coordinate. | 
| width | The width of the rectangle. | 
| height | The height of the rectangle. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method constructs an XRect object from a bottom left corner, a width and a height. It assumes that subsequent resizing and positioning operations on this object will also be based around the bottom left corner. As such the Pin property will remain at its default of Corner.BottomLeft. |  |  | 
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