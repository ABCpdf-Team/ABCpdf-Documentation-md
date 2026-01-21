---
title: "magnify"
css: "abcpdf-docs.css"
---

|  |  | Magnify Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Scale about a locked anchor point. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Magnify(double scaleX, double scaleY, double anchorX, double anchorY) ``` [Visual Basic] ``` Sub Magnify(scaleX As Double, scaleY As Double, anchorX As Double, anchorY As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| scaleX | The amount of horizontal scaling to apply. | 
| scaleY | The amount of vertical scaling to apply. | 
| anchorX | The horizontal coordinate about which the stretch should be applied. | 
| anchorY | The vertical coordinate about which the stretch should be applied. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method stretches the world space about a locked anchor point. Different degrees of horizontal and vertical stretch can be used. Another way of looking at this kind of transform is as a zoom. The anchor point is the location you're zooming in on and the scale factors indicate the level of zoom. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we add two chunks of text. The default text is added in black and the magnified text is drawn in red. We specify the middle of the document as the anchor point which means that all scaling is relative to the middle of the document. Our horizontal scale factor is larger than our text has been stretched horizontally somewhat. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(200, 200); doc.FontSize = 48; doc.AddText("Normal"); doc.FrameRect(); doc.Rect.Move(0, -100); doc.Color.String = "255 0 0"; doc.Transform.Magnify(2, 1.5, 302, 396); doc.AddText("Magnified"); doc.FrameRect(); doc.Save(Server.MapPath("transformmagnify.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(200, 200) doc.FontSize = 48 doc.AddText("Normal") doc.FrameRect() doc.Rect.Move(0, -100) doc.Color.String = "255 0 0" doc.Transform.Magnify(2, 1.5, 302, 396) doc.AddText("Magnified") doc.FrameRect() doc.Save(Server.MapPath("transformmagnify.pdf")) End Using ``` transformmagnify.pdf Also see example code in: Page GetBitmap Function, Page MakeFormXObject Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>