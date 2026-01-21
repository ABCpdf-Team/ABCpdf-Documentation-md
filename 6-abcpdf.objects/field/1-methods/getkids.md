---
title: "getkids"
css: "abcpdf-docs.css"
---

|  |  | GetKids Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets a set of Fields that are descendents of this one. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Field[] GetKids(int maximumDepth) ``` [Visual Basic] ``` Function GetKids(maximumDepth As Integer) As Field() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| maximumDepth | The maximum depth to search. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets a set of Fields that are descendents of this one. The maximum depth parameter allows you to control the depth to which the field tree is searched. One for immediate children, two for children and grandchildren, etc. Set the maximumDepth to Int32.MaxValue if you wish to retrieve all the fields under this one. |  |  | 
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