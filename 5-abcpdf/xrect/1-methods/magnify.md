---
title: "magnify"
css: "abcpdf-docs.css"
---

|  |  | Magnify Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Magnifies the rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Magnify(double x, double y) ``` [Visual Basic] ``` Sub Magnify(x As Double, y As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| x | The horizontal scale factor. | 
| y | The vertical scale factor. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Scales the rectangle width and height by a specified horizontal and vertical amount. When you magnify a rectangle one corner of the rectangle is pinned and the width and height of the rectangle adjusted. The corner which is pinned is indicated by the Pin property. The default pin corner is the bottom left. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code. [C#] ```csharp var rc = new XRect(); rc.String = "20 20 220 120"; Response.Write($"Rect = {rc}"); Response.Write(""); rc.Magnify(0.5, 0.5); Response.Write($"Scale = {rc}"); ``` [Visual Basic] ```vbnet Dim rc As New XRect() rc.String = "20 20 220 120" Response.Write($"Rect = {rc}") Response.Write("") rc.Magnify(0.5, 0.5) Response.Write($"Scale = {rc}") ``` Produces the following output. Rect = 20 20 220 120Scale = 20 20 120 70 Also see example code in: Doc AddImageDoc Function, Doc Transform Property, XImage Selection Property, XRendering AntiAliasText Property, XTextStyle HPos Property, XTextStyle VPos Property, PixMap SetAlpha Function, PixMap ToGrayscale Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>