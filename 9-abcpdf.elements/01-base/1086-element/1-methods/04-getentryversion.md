---
title: "04-getentryversion"
css: "abcpdf-docs.css"
---

|  |  | GetEntryVersion Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the minimum PDF version required for the use of a particular named entry. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual PDFVersion GetEntryVersion(string entry) ``` [Visual Basic] ``` Overridable Function GetEntryVersion(entry As string) As PDFVersion ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| entry | The name of the entry. | 
| return | The PDF version. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Get the minimum PDF version required for the use of a particular named entry. This function should be overridden by classes which inherit from this. They should provide return values for the entries specific to the new class. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>