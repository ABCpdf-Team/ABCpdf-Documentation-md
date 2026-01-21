---
title: "invert"
css: "abcpdf-docs.css"
---

|  |  | Invert Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Invert the transform. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Invert() ``` [Visual Basic] ``` Sub Invert() ``` |  |  | 
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
      
| When you invert a transform a rotation clockwise becomes an identical rotation anti-clockwise. A translation to the left becomes a translation to the right. A zoom in becomes a zoom out. Note that not every transform can be inverted. If you specify a magnification of zero you have shrunk your world space to a point. In this case it is not possible to invert the transform to get the original back again. However this kind of transform is uncommon in the real world and normally only occurs as a result of programming errors. If you apply the invert method to a non-invertable transform the transform will remain unmodified. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we add some text rotated at 45 degrees anti-clockwise around the middle of the document. We then invert the transform and draw some more text. Because the transform has been inverted the text now appears rotated 45 degrees clockwise. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 72; doc.Rect.String = "0 0 999 999"; doc.Pos.String = "302 396"; doc.Transform.Rotate(45, 302, 396); doc.AddText("45 Degrees"); doc.Pos.String = "302 396"; doc.Transform.Invert(); doc.AddText("Inverted"); doc.Save(Server.MapPath("transforminvert.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 72 doc.Rect.String = "0 0 999 999" doc.Pos.String = "302 396" doc.Transform.Rotate(45, 302, 396) doc.AddText("45 Degrees") doc.Pos.String = "302 396" doc.Transform.Invert() doc.AddText("Inverted") doc.Save(Server.MapPath("transforminvert.pdf")) End Using ``` transforminvert.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>