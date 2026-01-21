---
title: "runjs"
css: "abcpdf-docs.css"
---

|  |  | RunJS Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Run JavaScript code. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string RunJS(string js, JSOptions options) ``` [Visual Basic] ``` Function RunJS(js As String, options As JSOptions) As String ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| js | The JavaScript code to be executed. The method does nothing if it is null/Nothing or empty. | 
| options | The options. If it is null, a default will be used. | 
| return | The result of the execution converted to string. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method runs the JavaScript code against the PDF document. For example, you can execute actions that are executed when an annotation is clicked on by running the JavaScript code obtained with doc.GetInfo(annot.ID, "/A/JS:Text"). |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the JSOptions.SetUp event. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>