---
title: "equals"
css: "abcpdf-docs.css"
---

|  |  | Equals Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Test whether the two rectangles are effectively the same |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Equals(XRect other, double epsilon) bool Equals(XRect other) override bool Equals(object other) ``` [Visual Basic] ``` Function Equals(other As XRect, epsilon As Double) As Boolean Function Equals(other As XRect) As Boolean Overrides Function Equals(other As Object) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| other | The rect to test against. | 
| epsilon | The largest difference in values which will still be defined as equal | 
| return | Whether the two rects are the same. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Test whether the two rectangles are effectively the same. Rectangles are considered equal if they have the same position, width and height. This represents value equality for the rectangles in question. The underlying components of an XRect are represented as floating point numbers. Floating point numbers are subject to rounding errors, so there has to be a degree of latitude when comparing coordinate values. The degree of latitude is, by default, determined by the limitations defined in the PDF Specification. This is, broadly speaking, 5 decimal points so the default epsilon is typically 0.00001. However if you wish to rely on a specific epsilon value you should provide one. |  |  | 
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