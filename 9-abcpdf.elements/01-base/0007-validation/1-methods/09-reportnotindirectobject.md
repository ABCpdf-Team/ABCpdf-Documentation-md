---
title: "09-reportnotindirectobject"
css: "abcpdf-docs.css"
---

|  |  | ReportNotIndirectObject Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to report an object which should be indirect but is not. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ReportNotIndirectObject() ``` [Visual Basic] ``` Overridable Function ReportNotIndirectObject() As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| none |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to report an object which should be indirect but is not. Some entries are required to be indirect - to refer to an IndirectObject. For example Page objects are always indirect and a reference to a Page will always be made via a RefAtom. In the event that an object which is supposed to be indirect, is not, this function will be called. |  |  | 
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