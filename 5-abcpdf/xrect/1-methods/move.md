---
title: "move"
css: "abcpdf-docs.css"
---

|  |  | Move Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Translate the rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Move(double x, double y) ``` [Visual Basic] ``` Sub Move(x As Double, y As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| x | The horizontal distance to move the rectangle. | 
| y | The vertical distance to move the rectangle. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Moves the rectangle maintaining the width and height. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code. [C#] ```csharp var rc = new XRect(); rc.String = "20 20 220 120"; Response.Write($"Rect = {rc}"); rc.Move(50, 50); Response.Write(""); Response.Write($"Move = {rc}"); ``` [Visual Basic] ```vbnet Dim rc As New XRect() rc.String = "20 20 220 120" Response.Write($"Rect = {rc}") rc.Move(50, 50) Response.Write("") Response.Write($"Move = {rc}") ``` Produces the following output. Rect = 20 20 220 120Move = 70 70 270 170 Also see example code in: Doc AddColorSpaceSpot Function, XColor Alpha Property, XRendering AntiAliasText Property, XTextStyle CharSpacing Property, XTextStyle HPos Property, XTextStyle Justification Property, XTextStyle LeftMargin Property, XTextStyle LineSpacing Property, XTextStyle Outline Property, XTextStyle ParaSpacing Property, XTextStyle VPos Property, XTextStyle WordSpacing Property, XTransform Magnify Function, Page GetBitmap Function, PixMap SetAlpha Function, PixMap ToGrayscale Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>