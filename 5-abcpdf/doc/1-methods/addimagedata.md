---
title: "addimagedata"
css: "abcpdf-docs.css"
---

|  |  | AddImageData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Extract an image from data and add it to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddImageData(byte[] data) int AddImageData(byte[] data, int frame) ``` [Visual Basic] ``` Function AddImageData(data() As Byte) As Integer Function AddImageData(data() As Byte, frame As Integer) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| data | The data containing the image in a format such as JPEG or TIFF. | 
| frame | Some image types support multiple frames or pages. This is the one based index specifying the required frame (default one). | 
| return | The ID of the newly added Image Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Extract an image from a chunk of data and add it to the current page returning the ID of the newly added object. This method is essentially the same as AddImageFile but it allows you add images specified as raw data rather than as a file path. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: XRendering Overprint Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>