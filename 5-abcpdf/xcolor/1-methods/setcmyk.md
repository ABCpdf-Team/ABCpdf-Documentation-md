---
title: "setcmyk"
css: "abcpdf-docs.css"
---

|  |  | SetCmyk Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the color to an CMYK value. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetCmyk(int cyan, int magenta, int yellow, int black) void SetCmyk(int cyan, int magenta, int yellow, int black, int alpha) void SetCmyk(double cyan, double magenta, double yellow, double black) void SetCmyk(double cyan, double magenta, double yellow, double black, double alpha) ``` [Visual Basic] ``` Sub SetCmyk(cyan As Integer, magenta As Integer, yellow As Integer, black As Integer) Sub SetCmyk(cyan As Integer, magenta As Integer, yellow As Integer, black As Integer, alpha as Integer) Sub SetCmyk(cyan As Double, magenta As Double, yellow As Double, black As Double) Sub SetCmyk(cyan As Double, magenta As Double, yellow As Double, black As Double, alpha as Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| cyan | The amount of cyan (0 to 100). | 
| magenta | The amount of magenta (0 to 100). | 
| yellow | The amount of yellow (0 to 100). | 
| black | The amount of black (0 to 100). | 
| alpha | The level of opacity from transparent through to fully opaque (0 to 255). | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Set the color to CMYK and provide a value for it. Optionally set the alpha value to specify a transparency level. If this parameter is omitted the color is set to fully opaque - no transparency. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: Page GetBitmap Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>