---
title: "11-reportincorrectnumberofentries"
css: "abcpdf-docs.css"
---

|  |  | ReportIncorrectNumberOfEntries Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to report an array with an incorrect number of entries. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ReportIncorrectNumberOfEntries(int expected, int found) ``` [Visual Basic] ``` Overridable Function ReportIncorrectNumberOfEntries(expected As int, found As int) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| expected | The value which was expected. | 
| found | The value which was found. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to report an array with an incorrect number of entries. Some arrays have a set number of items. For example a value range may be represented as an array with two elements indicating higher and lower bounds. In the event that the number of entries is incorrect, this function will be called. |  |  | 
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