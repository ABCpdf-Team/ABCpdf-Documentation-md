---
title: "02-gettextrenderingmatrix"
css: "abcpdf-docs.css"
---

|  |  | GetTextRenderingMatrix Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the current Text Rendering Matrix (Trm). |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual XTransform GetTextRenderingMatrix(GraphicsState state) ``` [Visual Basic] ``` Overridable Function GetTextRenderingMatrix(state As GraphicsState) As XTransform ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| state | The current graphics state. | 
| return | The Text Rendering Matrix. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Get the current Text Rendering Matrix (Trm). This transformation matrix encompasses all text state parameters and can be used to place text for output. The Trm is part of the PDF Specification and is defined precisely in the documentation for this. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>