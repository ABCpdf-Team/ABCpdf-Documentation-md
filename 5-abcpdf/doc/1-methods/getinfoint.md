---
title: "getinfoint"
css: "abcpdf-docs.css"
---

|  |  | GetInfoInt Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets numeric information about an object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int GetInfoInt(int id, string type) ``` [Visual Basic] ``` Function GetInfoInt(id As Integer, type As String) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the object to be queried. | 
| type | The type of information to be retrieved. | 
| return | The returned integer. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function behaves identically to the GetInfo method but returns an integer rather than a string. If the information cannot be obtained or is not numeric, the return value will be zero. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the GetInfo function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>