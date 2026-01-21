---
title: "save"
css: "abcpdf-docs.css"
---

|  |  | Save Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Saves the PixMap to stream attempting to preserve resolution, color space and depth as far as the output format allows |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Save(string path) void Save(Stream stream, string name) ``` [Visual Basic] ``` Sub Save(path As String) Sub Save(stream As Stream, name As String) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The destination file path. | 
| stream | The destination output stream. | 
| name | A dummy file name used to determine the type of image required. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Saves the PixMap to stream attempting to preserve resolution, color space and depth as far as the output format allows. The output format is specified using a file extension. In the case of saving to file, the extension is taken from the file path. In the case of saving to stream, a dummy name should be provided. For details of the capabilities of output formats, see the XRendering.Save method. |  |  | 
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