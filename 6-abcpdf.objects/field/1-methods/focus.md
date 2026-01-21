---
title: "focus"
css: "abcpdf-docs.css"
---

|  |  | Focus Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Prepare document for drawing at the field location. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Focus() ``` [Visual Basic]`Function Focus() As Boolean` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | True if the focus operation was successful. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to focus on the field. This prepares the document for drawing at the field location. If the operation was successful then the function returns true. If the field has no visible location it will return false. The Doc.Page, Doc.Rect and Doc.Transform may all be changed as a result of calling this method. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: ABCpdf eForm Placeholder Example. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>