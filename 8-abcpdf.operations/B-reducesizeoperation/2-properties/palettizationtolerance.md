---
title: "palettizationtolerance"
css: "abcpdf-docs.css"
---

|  |  | PalettizationTolerance Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 0.01 | No | The amount of divergence from the target palette which will be allowed. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The amount of divergence from the target palette which will be allowed. Currently the only palette that is supported is RGB black and white. If an RGB image contains only grayscale components, and those grayscale pixels fit into the black and white palette with less than the amount of divergence specified, then it will be converted to one bit grayscale. The tolerance is measured in terms of the average distance between the colors of pixels and the color they would be converted to in the palette. Because the maximum distance varies depending on the number of components in the color space, this distance is then rescaled to a value between zero and one. Zero means that the pixels and the palette need to match exactly. One means all pixels will always match. Because this property results in a conversion to monochrome, monochrome settings will be used to compress the resultant image. See the MonochromImageDpi property for relevant notes. |  |  | 
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