---
title: "installlicense"
css: "abcpdf-docs.css"
---

|  |  | InstallLicense Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Install a license. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool InstallLicense(string license) ``` [Visual Basic] `Function InstallLicense(license As String) As Boolean` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| license | The license to install. | 
| return | True if a license is installed, otherwise false. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to install a license. Call this method at application startup before any ABCpdf objects have been created. You only need to call this method once though calling it additional times will not cause problems. Any license installed using this method will remain available to the current process (or application pool) until it unloads. Make sure you check the return value to ensure that the license has taken. If it has not, then report back the XSettings.LicenseDescription and the XSettings.Version. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See Manual Installation. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>