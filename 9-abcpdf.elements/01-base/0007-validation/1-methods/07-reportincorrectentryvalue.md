---
title: "07-reportincorrectentryvalue"
css: "abcpdf-docs.css"
---

|  |  | ReportIncorrectEntryValue Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to report an entry with an incorrect value. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ReportIncorrectEntryValue(string value) ``` [Visual Basic] ``` Overridable Function ReportIncorrectEntryValue(value As string) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| value | The incorrect value. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to report an entry with an incorrect value. Many entries have values which are constrained. For example some numbers may have a range between which they must fall. Some numbers may be cardinal only. Names are often used to indicated enumerated options. In the event that a value is incorrect this function will be called. |  |  | 
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