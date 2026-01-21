---
title: "enableapplicationreuse"
css: "abcpdf-docs.css"
---

|  |  | EnableApplicationReuse Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Enables an import application process to be reused so that it is terminated only manually or when this operation is disposed of. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool EnableApplicationReuse(ImportApplicationType app, bool reuse) ``` [Visual Basic]`Function EnableApplicationReuse(app As ImportApplicationType, reuse As Boolean) As Boolean` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| app | The import application. | 
| reuse | Whether the application process is to be reused. | 
| return | Whether the reuse status of the application has been changed. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function changes the reuse status of an application. Currently, the application processes of only Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be reused. Without application reuse, each call to ImportAny starts and terminates the application process. To avoid the overhead of the application start-up and exit, enable the reuse of the process for the particular application(s). The same process of that application is used in multiple calls to ImportAny of the same XpsImportOperation that uses the application. The reuse status is not changed if the process reuse of the application is not supported. If the process is running (for this XpsImportOperation object), the running process is terminated when its reuse is disabled. |  |  | 
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