---
title: "getscriptreturn"
css: "abcpdf-docs.css"
---

|  |  | GetScriptReturn Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Retrieves the client side onload script return value. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string GetScriptReturn(int id) ``` [Visual Basic]`Function GetScriptReturn(id As Integer) As String` |  |  | 
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
| return | The return value. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to retrieve the client side onload script return value. The ID should be obtained from a call to Doc.AddImageUrl or Doc.AddImageHtml. See the OnLoadScript property for further details. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the UseScript property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>