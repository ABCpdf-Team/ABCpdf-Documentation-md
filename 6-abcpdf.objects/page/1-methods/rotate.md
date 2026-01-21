---
title: "rotate"
css: "abcpdf-docs.css"
---

|  |  | Rotate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Rotates the page by a multiple of ninety degrees. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Rotate(int angle) ``` [Visual Basic] `Sub Rotate(angle As Integer)` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| angle | The number of degrees clockwise by which to rotate the page. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Rotates the page by a multiple of ninety degrees. By providing the Rotation property to this function you can derotate a page. The Rotation property and page bounding boxes (MediaBox, CropBox, BleedBox, TrimBox and ArtBox) will be adjusted to reflect the new viewing orientation. If a value is provided which is not a multiple of ninety degrees, an exception will be raised. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD height="55" vAlign=top class=sectheader>![](../../../images/steel-pin.gif)  

      Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>