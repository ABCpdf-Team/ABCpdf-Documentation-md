---
title: "setmeasureresolution"
css: "abcpdf-docs.css"
---

|  |  | SetMeasureResolution Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets the measurement resolutions. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetMeasureResolution(double dpi) void SetMeasureResolution(double dpiX, double dpiY) ``` [Visual Basic] ``` Sub SetMeasureResolution(dpi As Double) Sub SetMeasureResolution(dpiX As Double, dpiY As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| dpi | The new measurement resolution in DPI. | 
| dpiX | The new horizontal measurement resolution in DPI. | 
| dpiY | The new vertical measurement resolution in DPI. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Sets the measurement resolutions, which affects the measurements for certain output formats that does not support physical sizes. For example, SWF measurements are pixel-based while PDF measurements are in points (1/72 of an inch). This specifies how many pixels in SWF an inch in PDF represents. The values do not affect the pixel sizes of raster-image contents. If one of the values (dpiX or dpiY) is invalid, the other value may be used for both values. For SWF, these values are used only if XSaveOptions.Template is null. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we use 72 DPI so that 1 inch in PDF becomes 72 pixels in SWF. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); doc.SaveOptions.TemplateData = new XSaveTemplateData(); doc.SaveOptions.TemplateData.SetMeasureResolution(72); doc.Save(Server.MapPath("swfsave_mr.swf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) doc.SaveOptions.TemplateData = New XSaveTemplateData() doc.SaveOptions.TemplateData.SetMeasureResolution(72) doc.Save(Server.MapPath("swfsave_mr.swf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>