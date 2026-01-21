---
title: "01-stampannotation"
css: "abcpdf-docs.css"
---

|  |  | StampAnnotation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add stamp annotation to the current page of the doc. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp StampAnnotation(Doc doc, XRect rect, string caption, XColor color) ``` [Visual Basic] ``` StampAnnotation(doc As Doc, rect As XRect, caption As string, color As XColor) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | Doc | 
| rect | Annotation rectangle | 
| caption | The text of the stamp. | 
| color | The color of the stamp. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add stamp annotation to the current page of the doc. The supplied caption will be rendered in Helvetica Bold Oblique. The width of the provided rect will be adjusted to reflect the aspect ratio of the caption text. If you wish to maintain the original rect you can assign it to the Rect property after construction of the Stamp. |  |  | 
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