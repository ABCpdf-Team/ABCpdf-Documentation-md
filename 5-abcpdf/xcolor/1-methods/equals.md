---
title: "equals"
css: "abcpdf-docs.css"
---

|  |  | Equals Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Test whether the two colors are effectively the same |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Equals(XColor color) override bool Equals(object color) ``` [Visual Basic] ``` Function Equals(color As XColor) As Boolean Overrides Function Equals(other As Object) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| color | The color to test against. | 
| return | Whether the two colors are the same. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Test whether the two colors are effectively the same. Colors are considered equal if they have the same ColorSpace, the same number and values of color Components and the same Name. This represents value equality for the colors in question. The underlying components of a color are represented as floating point numbers. Floating point numbers are subject to rounding errors, so there has to be a degree of latitude when comparing color values. The degree of latitude is, by default, determined by the color space. CMYK values use a percentage based scale so the value used to determine the resolution of the comparison is 1%. Other color spaces use an eight bit scale so the resolution of comparison is 1/256. |  |  | 
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