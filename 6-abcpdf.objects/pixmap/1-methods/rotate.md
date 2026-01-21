---
title: "rotate"
css: "abcpdf-docs.css"
---

|  |  | Rotate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Rotate the image clockwise |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Rotate(int degrees) ``` [Visual Basic] ``` Sub Rotate(degrees As Integer) ``` `may throw ArgumentOutOfRangeException()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| degrees | The number of degrees clockwise that the image should be rotated. This must be a multiple of 90. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function rotates the PixMap image clockwise. The rotation angle must be a multiple of 90. If an invalid number of degrees is specified, then an ArgumentOutOfRangeException will be thrown. An image may have an associated bit mask or soft (alpha) mask. If this is the case, the associated mask will be transformed as well.When a PixMap is drawn on a page, it is scaled to fit into a particular location. The scaling is separate from the PixMap itself. Rotating by 90 or 270 degrees will swap the width and height of the PixMap. Because the scaling of drawn copies is separate from the PixMap itself, any previously drawn instances of the PixMap may appear to have an incorrect aspect ratio.After the Bitmap has been set, the PixMap will be uncompressed. You may wish to compress it using a call like CompressJpeg or CompressFlate. |  |  | 
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