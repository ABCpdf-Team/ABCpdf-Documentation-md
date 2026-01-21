---
title: "flip"
css: "abcpdf-docs.css"
---

|  |  | Flip Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Flip the image horizontally or vertically |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Flip(bool horizontal, bool vertical) ``` [Visual Basic] ``` Sub Flip(horizontal As Boolean, vertical As Boolean) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| horizontal | Whether to flip the image horizontally. | 
| vertical | Whether to flip the image vertically | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function flips the image horizontally or vertically or both. Flipping both horizontally and vertically is equivalent to a 180 degree rotation.An image may have an associated bit mask or soft (alpha) mask. If this is the case the associated mask will be transformed as well.Flipping horizontally will mean that pixels that were on the far right of the image will be moved to the far left and pixels on the left will be moved to the right.Flipping horizontally will mean that pixels that were on the top of the image will be moved to the bottom and pixels that were on the bottom will be moved to the top. After the Bitmap has been set the PixMap will be uncompressed. You may wish to compress it using a call like CompressJpeg or CompressFlate. |  |  | 
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