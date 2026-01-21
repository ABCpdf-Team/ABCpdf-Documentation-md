---
title: "setfile"
css: "abcpdf-docs.css"
---

|  |  | SetFile Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the raw binary content of the stream using data from a file. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetFile(string path) ``` [Visual Basic] ``` Sub SetFile(path As String) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | A path to a file containing data which should be placed in the StreamObject. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Set the raw binary content of the stream using data read from a file. If the file cannot be read then an exception is thrown. Compression settings are unaltered. So if - for example - you have a stream which is Flate compressed you must use SetFile with Flate compressed data. For this reason you may wish to call ClearData before using SetFile. |  |  | 
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