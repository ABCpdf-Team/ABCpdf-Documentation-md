---
title: "12-reportexception"
css: "abcpdf-docs.css"
---

|  |  | ReportException Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to report an Exception that was thrown during validation. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ReportException(Element element, Exception ex) ``` [Visual Basic] ``` Overridable Function ReportException(element As Element, ex As Exception) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| element | The Element which was being processed. | 
| ex | The Exception which was thrown. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to report an Exception that was thrown during validation. In general you do not want the validation of one Element to affect another. So if an Exception is thrown during the validation of one Element, you want this to be reported, but then for validation to continue. In the event that this happens, this function will be called. |  |  | 
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