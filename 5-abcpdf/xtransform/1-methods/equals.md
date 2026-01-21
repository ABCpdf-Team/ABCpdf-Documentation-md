---
title: "equals"
css: "abcpdf-docs.css"
---

|  |  | Equals Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Determines if two transforms are effectively the same. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Equals(XTransform other, double epsilon) bool Equals(XTransform other) override bool Equals(object other) ``` [Visual Basic] ``` Function Equals(other As XTransform, epsilon As Double) As Boolean Function Equals(other As XTransform) As Boolean Overrides Function Equals(other As Object) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| other | The transform to be compared against this one | 
| epsilon | The largest difference in values which will still be defined as equal | 
| return | Whether the two transforms are the same. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Determines if two transforms are effectively the same. Transforms contain a set of elements which are represented as floating point numbers. Floating point numbers are subject to rounding errors so the epsilon value is used to determine the resolution of the comparison. Only if two elements differ by more than the value of epsilon will they be defined as not equal. Internally Acrobat uses double precision floating point numbers for a very high level of accuracy. However within a PDF itself these numbers are typically only represented to around five decimal points. You may wish to represent similar levels of accuracy in your epsilon values. The default epsilon is zero so by default, transforms have to match perfectly for them to be considered equal. |  |  | 
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