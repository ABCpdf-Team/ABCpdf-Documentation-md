---
title: "resample"
css: "abcpdf-docs.css"
---

|  |  | Resample Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Changes the number of bits per color component. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Resample(int bitsPerComponent) ``` [Visual Basic]`Sub Resample(bitsPerComponent As Integer)` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| bitsPerComponent | The number of bits per color component. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Change the number of bits per color component. The bit depths you should use are 1, 2, 4, 8 or 16. Other values are not supported in the PDF Specification. Changing this property for Indexed color images changes the precision of the index rather than of the color components. If you want to change the precision of the components you need to Realize the PixMap first. Operations like Resize operate more naturally on eight and sixteen bit images - producing better results, faster, using less memory. So if you will be resizing and also moving to eight or sixteen bit depth it is typically better to Resample before calling Resize. After this method is called the image may no longer be longer compressed. You may wish to compress it using the StreamObject.Compress method. |  |  | 
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