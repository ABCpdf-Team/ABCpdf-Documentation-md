---
title: "position"
css: "abcpdf-docs.css"
---

|  |  | Position Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Position the bottom left of the rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Position(double x, double y) void Position(double x, double y, Corner corner) ``` [Visual Basic] ``` Sub Position(x As Double, y As Double) Sub Position(x As Double, y As Double, corner As Corner) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| x | The new left position. | 
| y | The new bottom position. | 
| corner | The corner to position. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Moves the rectangle to the supplied position while maintaining the width and height. The corner moved to the location is indicated by the Pin property but you can override this default by specifying a corner when calling this function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code. [C#] ```csharp var rc = new XRect(); rc.String = "20 20 220 120"; Response.Write($"Rect = {rc}"); Response.Write(""); rc.Position(50, 50); Response.Write($"Pos. = {rc}"); ``` [Visual Basic] ```vbnet Dim rc As New XRect() rc.String = "20 20 220 120" Response.Write($"Rect = {rc}") Response.Write("") rc.Position(50, 50) Response.Write($"Pos. = {rc}") ``` Produces the following output. Rect = 20 20 220 120Pos. = 50 50 250 150 Also see example code in: Doc AddImageDoc Function, Doc TopDown Property, Doc Transform Property, XImage Selection Property, XTransform Skew Function, XTransform Translate Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>