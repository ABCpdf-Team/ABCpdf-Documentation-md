---
title: "addpie"
css: "abcpdf-docs.css"
---

|  |  | AddPie Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a pie slice to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddPie(double angleStart, double angleEnd, bool filled) ``` [Visual Basic]`Function AddPie(angleStart As Double, angleEnd As Double, filled As Boolean) As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| angleStart | The start angle of the pie slice in degrees. | 
| angleEnd | The end angle of the pie slice in degrees. | 
| filled | Whether to fill the pie slice rather than simply outline it. | 
| return | The Object ID of the newly added Graphic Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a pie slice to the current page. The slice is drawn in the current color at the current width and with the current options. The pie slice represents a segment of the oval which would fill the current rectangle. Drawing starts at the start angle and the arc is swept out until the end angle is reached. Angles are measured anti-clockwise with zero at three o'clock. The slice may be outlined or filled depending on the values passed to the function. The AddPie function returns the Object ID of the newly added Graphic Object. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds two pie slices to a document. [C#] ```csharp using var doc = new Doc(); doc.Width = 80; doc.Rect.Inset(50, 50); doc.Color.String = "255 0 0"; doc.AddPie(0, 90, true); doc.Color.String = "0 255 0"; doc.AddPie(180, 270, false); doc.Save(Server.MapPath("docaddpie.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Width = 80 doc.Rect.Inset(50, 50) doc.Color.String = "255 0 0" doc.AddPie(0, 90, True) doc.Color.String = "0 255 0" doc.AddPie(180, 270, False) doc.Save(Server.MapPath("docaddpie.pdf")) End Using ``` docaddpie.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>