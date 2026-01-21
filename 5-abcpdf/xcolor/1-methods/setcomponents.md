---
title: "setcomponents"
css: "abcpdf-docs.css"
---

|  |  | SetComponents Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the color to a set of ColorSpace PDF components |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetComponents(double value1) void SetComponents(double value1, double value2) void SetComponents(double value1, double value2, double value3) void SetComponents(double value1, double value2, double value3, double value4) ``` [Visual Basic] ``` Sub SetComponents(value1 As Double) Sub SetComponents(value1 As Double, value2 As Double) Sub SetComponents(value1 As Double, value2 As Double, value3 As Double) Sub SetComponents(value1 As Double, value2 As Double, value3 As Double, value4 As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| value1 | The intensity of the first component (typically 0 to 1) | 
| value2 | The intensity of the second component (typically 0 to 1) | 
| value3 | The intensity of the third component (typically 0 to 1) | 
| value4 | The intensity of the fourth component (typically 0 to 1) | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Sets the color to the generic ColorSpace color space and provide a set of components for it. PDF color components typically range between zero - no intensity - and one - 100% intensity. However this is not always the case. For color spaces such as Lab the components may take a wider range of values. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: ColorSpace Gamma Property, ColorSpace WhitePoint Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>