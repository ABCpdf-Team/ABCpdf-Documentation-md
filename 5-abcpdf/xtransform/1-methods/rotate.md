---
title: "rotate"
css: "abcpdf-docs.css"
---

|  |  | Rotate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Rotate about a locked anchor point (angle in degrees). |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Rotate(double angle, double anchorX, double anchorY) ``` [Visual Basic] ``` Sub Rotate(angle As Double, anchorX As Double, anchorY As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| angle | The angle to rotate in degrees. | 
| anchorX | The horizontal coordinate about which the rotation should be applied. | 
| anchorY | The vertical coordinate about which the rotation should be applied. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method rotates the world space about a locked anchor point. The angle is specified in degrees anti-clockwise. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we add a number of chunks of text rotated at different angles about the middle of the document. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 48; doc.TextStyle.Indent = 48; for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 48 doc.TextStyle.Indent = 48 Dim i As Integer = 1 While i rotate.pdf Also see example code in: ABCpdf Landscape Example, Doc AddGrid Function, Doc AddXObject Function, Doc Transform Property, XTransform Invert Function, XTransform Reset Function, XTransform AngleUnit Property, FontObject Widths Property, Page Rotation Property, XpsImportOperation Import Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>