---
title: "loadcolorbooks"
css: "abcpdf-docs.css"
---

|  |  | LoadColorBooks Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Load color books for use when rendering spot color images. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void LoadColorBooks(string path) ``` [Visual Basic] `Sub LoadColorBooks(path As String)` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The file to load or directory to scan. | 
| return | None. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adobe Photoshop multichannel PSD files sometimes reference named spot colors that are defined in color books Without the original color book it is not possible to convert these images accurately because the name of a color does not tell you what it looks like. The only way to know is to find the original color book and use the information that is found there. ABCpdf will attempt to locate color books on your system but you can provide it with help by calling this function. Pass in either a path to a file you would like to load, or a path to a directory of files that you would like to load. The named colors are held on a global basis so there is no need to repeat the call unless the files change. ABCpdf currently supports color books in .acb - Adobe Color Book format. |  |  | 
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