---
title: "addgrid"
css: "abcpdf-docs.css"
---

|  |  | AddGrid Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a visible grid to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddGrid() ``` [Visual Basic] ``` Function AddGrid() As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | The Object ID of the newly added Grid Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a visible grid to the current page. The grid shows locations on the page and the effect of the current transform. It is designed to help with object positioning during development. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code modifies the page transform and then adds a grid to show how the transform has affected the page. [C#] ```csharp using var doc = new Doc(); doc.Page = doc.AddPage(); doc.Transform.Rotate(20, 100, 100); doc.AddGrid(); doc.Save(Server.MapPath("docaddgrid.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Page = doc.AddPage() doc.Transform.Rotate(20, 100, 100) doc.AddGrid() doc.Save(Server.MapPath("docaddgrid.pdf")) End Using ``` docaddgrid.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>