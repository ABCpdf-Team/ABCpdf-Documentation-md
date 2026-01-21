---
title: "transformpoints"
css: "abcpdf-docs.css"
---

|  |  | TransformPoints Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Applies this transform to a specified array of points. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp override Point[] TransformPoints(Point[] points) override PointF[] TransformPoints(PointF[] points) override XPoint[] TransformPoints(XPointF points) ``` [Visual Basic] ``` Overrides Sub TransformPoints(points As Point()) As Point[] Overrides Sub TransformPoints(points As PointF()) As PointF[] Overrides Sub TransformPoints(points As XPoint()) As XPoint[] ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| points | The array of points to be transformed. | 
| return | The array that was passed in. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Applies this transform to a specified array of points. The behavior of this method is the same as that of the System.Drawing.Drawing2D Matrix.TransformPoints function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
|  |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>