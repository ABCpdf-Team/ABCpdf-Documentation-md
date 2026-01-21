---
title: "fitin"
css: "abcpdf-docs.css"
---

|  |  | FitIn Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Fits the rectangle as content inside another rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void FitIn(XRect rect, ContentAlign align, ContentScaleMode scaleMode) ``` [Visual Basic] ``` Sub FitIn(rect As XRect, align As ContentAlign, scaleMode As ContentScaleMode) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| rect | The containing rectangle. | align | The content alignment. | scaleMode | The content scale mode. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The rectangle is fitted inside the containing rectangle. The ContentAlign enumeration can take a combination of the following values: Center Left Right Top Bottom The ContentScaleMode enumeration can take any of the following values: ShowAll – make the content the biggest and completely within the area while keeping the aspect ratio. NoBorder – make the content the smallest and covering the entire area while keeping the aspect ratio. ExactFit – scale the content possibly with distortion to fit the entire area. It is the same as assignment. NoScale – no scaling. The rectangle is repositioned. |  |  | 
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