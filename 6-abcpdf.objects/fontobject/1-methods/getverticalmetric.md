---
title: "getverticalmetric"
css: "abcpdf-docs.css"
---

|  |  | GetVerticalMetric Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the vertical metric for a character. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual VerticalMetric GetVerticalMetric(int code) ``` [Visual Basic] ``` Overridable Function GetVerticalMetric(code As int) As VerticalMetric ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| code | The native character code to get metrics for. | 
| return | The vertical metrics. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Get the vertical metric for a character indexed by native character code. The VerticalMetric structure consists of: Position - a vector or point used for positioning the glyph. Displacement - a vector or point to use for advancing the current text insertion point so that the next glyph can be positioned Vertical metrics are only used when the IsVertical property is true. |  |  | 
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