---
title: "union"
css: "abcpdf-docs.css"
---

|  |  | Union Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Union this rectangle with another rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Union(XRect rect) void Union(XRect rect, bool noAreaIsEmpty) ``` [Visual Basic] ``` Sub Union(rect As XRect) Sub Union(rect As XRect, noAreaIsEmpty as Boolean) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| rect | The rectangle to add to this one. The supplied rectangle is left unchanged by this function. | 
| noAreaIsEmpty | Whether to treat rectangles with no area as empty - default true. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Union the rectangle with another rectangle. This rectangle becomes the smallest rectangle that encloses both rectangles. Rectangles with no area will, by default, be treated as being empty. A union of a non-empty rectangle with an empty rectangle always results in the output being set to the non-empty rectangle value. If both rectangles are empty this rectangle will be left unchanged. If the noAreaIsEmpty parameter is set to false then rectangles with no area will be treated as points and the output union will include that point. |  |  | 
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