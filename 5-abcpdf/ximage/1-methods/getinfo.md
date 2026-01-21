---
title: "getinfo"
css: "abcpdf-docs.css"
---

|  |  | GetInfo Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets internal information from the image. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string GetInfo(string type) ``` [Visual Basic] ``` Function GetInfo(type As String) As String ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| type | The type of information to get. | 
| returns | The information. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets internal information from the image. Internal information is format specific so you need to use different selectors with different formats. The JPEG 2000 format implements a "Structure" info which provides the tag structure of the raw data together with types, offsets and lengths. This can be used to modify or insert tags for custom output. The TIFF format implements a "TiffTag:" info which allows you to get the values of TIFF tags either by name or number. Simply append the item you are interested in. For example you might use "TiffTag:InkNames" to get the ink or "TiffTag:271" to retrieve the scanner manufacturer. |  |  | 
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