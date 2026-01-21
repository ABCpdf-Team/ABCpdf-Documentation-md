---
title: "getinfodate"
css: "abcpdf-docs.css"
---

|  |  | GetInfoDate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets date information about an object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp DateTime GetInfoDate(int id, string type) DateTime GetInfoDate(int id, string type, bool allowLocal) ``` [Visual Basic] ``` Function GetInfoDate(id As Integer, type As String) As DateTime Function GetInfoDate(id As Integer, type As String, allowLocal As Boolean) As DateTime ``` |  |  | 
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
| allowLocal | For dates containing time zone information, if the parameter is true, the returned values will be local times (local to the time zone of the dates, and not to the local machine); if the parameter is false, the returned values will be UTC times. The default is false. | 
| return | The returned value. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function behaves identically to the GetInfo method but returns a DateTime rather than a string. If the information cannot be obtained or is not a date, then the return value will be the zero DateTime. PDF dates also contain times. They are stored as strings in PDF so this function is mostly used with the :Text object type. |  |  | 
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