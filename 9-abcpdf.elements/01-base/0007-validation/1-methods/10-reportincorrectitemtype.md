---
title: "10-reportincorrectitemtype"
css: "abcpdf-docs.css"
---

|  |  | ReportIncorrectItemType Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to report an object which is of the wrong type. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ReportIncorrectItemType(string expectedType, string actualType, Atom atom) ``` [Visual Basic] ``` Overridable Function ReportIncorrectItemType(expectedType As string, actualType As string, atom As Atom) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| expectedType | The expected type name. | 
| actualType | The actual type name. | 
| atom | The atom which was found. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to report an object which is of the wrong type. Some entries are required to specific types of object. For example a Page Node has children which must be either other Page Nodes or Pages. If an item like this is retrieved, and turns out to be a different type, this function will be called. |  |  | 
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