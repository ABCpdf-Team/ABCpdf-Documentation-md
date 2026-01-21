---
title: "getpath"
css: "abcpdf-docs.css"
---

|  |  | GetPath Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the path to the file for the specified platform |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string GetPath(string platform) ``` [Visual Basic] ``` Function GetPath(platform As String) As String ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| platform | The platform name. | 
| return | The file path. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method is provided for low level control over obsolete entries contained in old PDF documents. So in general you should be using the Rationalize method and the Uri property rather than this method. A FileSpecification may hold multiple paths to a file. Each path is specific to a platform such as Mac, Windows or Unix. For further details see the Platform property. This function allolws you to retrieve the path for the specified platform. If there is no matching path then null will be returned. |  |  | 
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