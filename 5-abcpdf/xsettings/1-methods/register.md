---
title: "register"
css: "abcpdf-docs.css"
---

|  |  | Register Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Register and install a trial license. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Register() ``` [Visual Basic]`Sub Register()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | None. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to register ABCpdf and install a trial license if no license is installed. You should never need to call this method as both the process of installing and the process of running the PDFSettings application will automatically register ABCpdf. If for some reason the registration fails, all you need to do is run the PDFSettings application as Administrator. Part of registration includes setting up ABCpdf as an event source for the Windows Event Log. However this can only be done when running as Administrator. If you do not have Administrator rights then events can be logged but the text associated with them will be tagged "The description for Event ID 4096 from source ABCpdf cannot be found." |  |  | 
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