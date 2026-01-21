---
title: "3-fromsides"
css: "abcpdf-docs.css"
---

|  |  | FromSides Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Creates an XRect from the coordinates of two diagonally opposite corners. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static XRect FromSides(double xMin, double yMin, double xMax, double yMax) ``` [Visual Basic] ``` Shared Function FromSides(xMin As Double, yMin As Double, xMax As Double, yMax As Double) As XRect ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| xMin | The minimum x coordinate. | 
| yMin | The minimum y coordinate. | 
| xMax | The maximum x coordinate. | 
| yMax | The maximum y coordinate. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method constructs an XRect object from the coordinates of two diagonally opposite corners. If the minimum x values are larger than the minimum x values then the XRect will have a negative width. Similarly if the minimum y values are larger than the maximum y values then the XRect will have a negative height. |  |  | 
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