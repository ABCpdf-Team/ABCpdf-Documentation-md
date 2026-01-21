---
title: "gethttpstatuscode"
css: "abcpdf-docs.css"
---

|  |  | GetHttpStatusCode Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Retrieves the HTTP status code. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int GetHttpStatusCode(int id) ``` [Visual Basic]`Function GetHttpStatusCode(id As Integer) As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the web page to be accessed. | 
| return | The HTTP status code or zero if not available. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to retrieve the HTTP status code if the URL uses the HTTP protocol. The ID should be obtained from a call to Doc.AddImageUrl. If the PageLoadMethod property is WebBrowserNavigate, only error status codes are available. Non-error status codes, such as 200, are not available. |  |  | 
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