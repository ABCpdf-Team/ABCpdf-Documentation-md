---
title: "setrgb"
css: "abcpdf-docs.css"
---

|  |  | SetRgb Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the color to an RGB value. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetRgb(int red, int green, int blue) void SetRgb(int red, int green, int blue, int alpha) void SetRgb(double red, double green, double blue) void SetRgb(double red, double green, double blue, double alpha) ``` [Visual Basic] ``` Sub SetRgb(red As Integer, green As Integer, blue As Integer) Sub SetRgb(red As Integer, green As Integer, blue As Integer, alpha as Integer) Sub SetRgb(red As Double, green As Double, blue As Double) Sub SetRgb(red As Double, green As Double, blue As Double, alpha as Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| red | The amount of red (0 to 255). | 
| green | The amount of green (0 to 255). | 
| blue | The amount of blue (0 to 255). | 
| alpha | The level of opacity from transparent through to fully opaque (0 to 255). | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Set the color to RGB and provide a value for it. Optionally set the alpha value to specify a transparency level. If this parameter is omitted the color is set to fully opaque - no transparency. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: Doc AddXObject Function, Doc String Property, Page GetBitmap Function, ImageOperation GetImageProperties Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>