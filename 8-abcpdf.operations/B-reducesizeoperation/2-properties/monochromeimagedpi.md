---
title: "monochromeimagedpi"
css: "abcpdf-docs.css"
---

|  |  | MonochromeImageDpi Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 150.0 | No | The target resolution for the resampling of monochrome images. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The target resolution for the resampling of monochrome images. Most monochrome images are black and white. When the CompressImages setting is set this option is used to determine the resolution at images in this color space should be targeted. Images are scaled down if they are too large but not up if they are too small. Monochrome images compress extremely well so even large images are small in data size. However resizing monochrome images requires that a nearest neighbor approach is used and this can result in a reduction in image quality that can be quite noticeable. When this happens you will see that images may become choppy and words fragmented and indistinct. The alternative here is to convert to grayscale but that produces a larger data size as it is much less compressible. For this reason you may wish to increase the default DPI setting as the default set here is quite aggressive. |  |  | 
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