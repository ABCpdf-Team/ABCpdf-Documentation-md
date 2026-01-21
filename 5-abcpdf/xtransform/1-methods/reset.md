---
title: "reset"
css: "abcpdf-docs.css"
---

|  |  | Reset Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Reset to the identity. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Reset() ``` [Visual Basic] ``` Sub Reset() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| None |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method resets the transform to it's original state. This state is known as the identity and indicates that no transformation will be applied. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we add some text rotated at 60 degrees around the middle of the document. We then reset the transform and draw some more text. This text is drawn with no rotation because the transform has been reset. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(10, 10); doc.FontSize = 96; doc.Transform.Rotate(60, 302, 396); doc.Pos.String = "302 396"; doc.AddText("Angled"); doc.FrameRect(); doc.Transform.Reset(); doc.Pos.String = "302 396"; doc.AddText("Reset"); doc.FrameRect(); doc.Save(Server.MapPath("transformreset.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(10, 10) doc.FontSize = 96 doc.Transform.Rotate(60, 302, 396) doc.Pos.String = "302 396" doc.AddText("Angled") doc.FrameRect() doc.Transform.Reset() doc.Pos.String = "302 396" doc.AddText("Reset") doc.FrameRect() doc.Save(Server.MapPath("transformreset.pdf")) End Using ``` transformreset.pdf Also see example code in: XTransform Rotate Function, FontObject Widths Property, Page GetBitmap Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>