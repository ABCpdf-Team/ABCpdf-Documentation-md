---
title: "translate"
css: "abcpdf-docs.css"
---

|  |  | Translate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Translate horizontally and vertically. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Translate(double x, double y) ``` [Visual Basic] ``` Sub Translate(x As Double, y As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| x | The distance to translate to the right. | 
| y | The distance to translate upwards. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method shifts the world space a specified distance up and to the right. Objects on the PDF will appear to translate upwards and to the right. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we draw two rectangles into our document. The black rectangle is drawn before the translation operation and the red one is drawn after it. [C#] ```csharp using var doc = new Doc(); doc.Rect.Width = 200; doc.Rect.Height = 250; doc.Rect.Position(100, 100); doc.Width = 20; doc.FrameRect(); doc.Transform.Translate(200, 200); doc.Color.String = "255 0 0"; // red doc.FrameRect(); doc.Save(Server.MapPath("transformtranslate.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Width = 200 doc.Rect.Height = 250 doc.Rect.Position(100, 100) doc.Width = 20 doc.FrameRect() doc.Transform.Translate(200, 200) doc.Color.String = "255 0 0" ' red doc.FrameRect() doc.Save(Server.MapPath("transformtranslate.pdf")) End Using ``` transformtranslate.pdf Also see example code in: ABCpdf Landscape Example, Page GetBitmap Function, Page Rotation Property, XpsImportOperation Import Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>