---
title: "getinfodouble"
css: "abcpdf-docs.css"
---

|  |  | GetInfoDouble Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets numeric information about an object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp double GetInfoDouble(int id, string type) ``` [Visual Basic] ``` Function GetInfoDouble(id As Integer, type As String) As Double ``` |  |  | 
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
| return | The returned value. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function behaves identically to the GetInfo method but returns a double rather than a string. If the information cannot be obtained or is not numeric, the return value will be zero. |  |  | 
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