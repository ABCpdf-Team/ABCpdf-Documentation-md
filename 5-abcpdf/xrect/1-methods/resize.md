---
title: "resize"
css: "abcpdf-docs.css"
---

|  |  | Resize Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Resizes the rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Resize(double w, double h) void Resize(double w, double h, Corner corner) ``` [Visual Basic] ``` Sub Resize(w As Double, h As Double) Sub Resize(w As Double, h As Double, corner as Corner) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| w | The new width. | 
| h | The new height. | 
| corner | The corner to pin. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Changes the width and height of the rectangle while maintaining the position. When you change the width or height of a rectangle one corner of the rectangle is pinned to maintain position. The corner which is pinned is indicated by the Pin property but you can override this default by specifying a corner when calling this function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code. [C#] ```csharp var rc = new XRect(); rc.String = "20 20 220 120"; Response.Write($"Rect = {rc}"); Response.Write(""); rc.Resize(50, 150); Response.Write($"Pos. = {rc}"); ``` [Visual Basic] ```vbnet Dim rc As New XRect() rc.String = "20 20 220 120" Response.Write($"Rect = {rc}") Response.Write("") rc.Resize(50, 150) Response.Write($"Pos. = {rc}") ``` Produces the following output. Rect = 20 20 220 120Pos. = 20 20 70 170 Also see example code in: ABCpdf Text Flow Round Image Example. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>