---
title: "getapplicationfolder"
css: "abcpdf-docs.css"
---

|  |  | GetApplicationFolder Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the installation folder of an import application. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static string GetApplicationFolder(ImportApplicationType app) ``` [Visual Basic]`Shared Function GetApplicationFolder(app As ImportApplicationType) As String` |  |  | 
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
| return | The installation folder of the application. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function returns the installation folder of an application that can be used by ImportAny. The installation folder of ImportApplicationType.ShellAssociation is null. For the Microsoft Office applications, it will be the Microsoft Office installation folder. If this function returns null for an application other than ShellAssociation, it means that the application is not installed or that ABCpdf has failed to find the application. If this is the case, ImportAny will fail. Before calling ImportAny, you can use this function to make sure that ABCpdf finds the application. |  |  | 
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