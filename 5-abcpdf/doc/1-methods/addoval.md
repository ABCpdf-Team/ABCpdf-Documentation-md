---
title: "addoval"
css: "abcpdf-docs.css"
---

|  |  | AddOval Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds an oval to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddOval(bool filled) ``` [Visual Basic]`Function AddOval(filled As Boolean) As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| filled | Whether to fill the oval rather than simply outline it. | 
| return | The Object ID of the newly added Graphic Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds an oval to the current page. The oval is drawn in the current color at the current width and with the current options. It is scaled to fill the current rectangle. The oval may be outlined or filled. The AddOval function returns the Object ID of the newly added Graphic Object. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds two ovals to a document. The outline oval is semi-transparent. [C#] ```csharp using var doc = new Doc(); doc.Width = 80; doc.Rect.Inset(50, 50); doc.Color.String = "255 0 0"; doc.AddOval(true); doc.Color.String = "0 255 0 128"; doc.AddOval(false); doc.Save(Server.MapPath("docaddoval.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Width = 80 doc.Rect.Inset(50, 50) doc.Color.String = "255 0 0" doc.AddOval(True) doc.Color.String = "0 255 0 128" doc.AddOval(False) doc.Save(Server.MapPath("docaddoval.pdf")) End Using ``` docaddoval.pdf Also see example code in: XColor Components Property, ColorSpace Gamma Property, ColorSpace WhitePoint Property, SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>