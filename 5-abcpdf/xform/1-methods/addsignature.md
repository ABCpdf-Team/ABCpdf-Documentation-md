---
title: "addsignature"
css: "abcpdf-docs.css"
---

|  |  | AddSignature Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add unsigned signature field. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Signature AddSignature(XRect rect, string name) Signature AddSignature(XRect rect, string name, bool minimal) ``` [Visual Basic] ``` Function AddSignature(rect As XRect, name As string) As Signature Function AddSignature(rect As XRect, name As string, minimal As Boolean) As Signature ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| rect | Rectangle of the form field | 
| name | Name of the form field | 
| minimal | Whether to add a minimal signature (default false) | 
| return | Form field object | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add unsigned signature field. To add an invisible field provide an empty rectangle. By default we add a maximal signature rather than a minimal one - one with placeholder values where elements are still to be completed. This minimizes the number of changes during an incremental update and means that Acrobat is less likely to complain about a change it does not understand. However while this may be good for Acrobat, other less capable software may not be able to tell the difference between a placeholder and a real value and may be confused. In this type of situation you may wish to add a minimal signature containing only those elements that are absolutely necessary. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Annotations example project. None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>