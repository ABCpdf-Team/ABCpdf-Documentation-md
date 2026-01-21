---
title: "preservekoptions"
css: "abcpdf-docs.css"
---

|  |  | PreserveKOptions Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Write | Description | 
| **[C#]** ```csharp BlackPreservation ``` [Visual Basic] `BlackPreservation` | Intent | Yes | Determines how color transforms preserve black when recoloring to CMYK. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Tell the color management system how to preserve black (K) when converting color to CMYK. Normal color transforms first convert to device independent XYZ using the source profile, then from XYZ to the destination space using the destination profile. Since CMYK is an overdetermined colorspace, an XYZ intermediate value can be converted into a number of different and equivalent CMYK values. The XRendering.BlackPreservation enumeration may take the following values: Off - Do not attempt to preserve black when transforming. Intent - Use special rendering intents to preserve black - must be supported by the ICC profile. Plane - for CMYK to CMYK transforms only; run CMY through the profile, do not change K. See also the XRendering.PreserveKOptions property. |  |  | 
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