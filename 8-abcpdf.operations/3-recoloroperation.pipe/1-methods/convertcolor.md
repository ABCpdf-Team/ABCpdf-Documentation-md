---
title: "convertcolor"
css: "abcpdf-docs.css"
---

|  |  | ConvertColor Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Convert color components from the source color space to the destination one. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Recolor(double[] from, double[] to) ``` [Visual Basic] ``` Sub Recolor(from as Double(), to As Double()) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| from | An array of source color components. The number of items in the array should be equal to the number of components in the source color space. | 
| to | An array of destination color components which will be updated with the values. The number of items in the array should be equal to the number of components in the destination color space. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Convert color components from the source color space to the destination one. Color components typically vary between zero and one representing the intensity of each component. So a high intensity green in the RGB color space might be represented as [0.0 1.0 0.0]. You need to ensure that the arrays you pass are the right size. So for example a conversion from RGB to CMYK would need a from array of size three and a to array of size four. If the arrays are incorrectly sized then an exception will be thrown. |  |  | 
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