---
title: "installsystemlicense"
css: "abcpdf-docs.css"
---

|  |  | InstallSystemLicense Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Install a system license. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool InstallSystemLicense(stirng license) ``` [Visual Basic]`Function InstallSystemLicense(license As String) As Boolean` |  |  | 
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
      
| Use this method to install a system license. Call this method at application startup before any ABCpdf objects have been created. This method saves the license for use on a system-wide basis. So, once a license is successfully installed, it will stay on the system and be picked up by ABCpdf automatically. Licenses are specific to the process model so licenses installed for with 32-bit ABCpdf will not be available to 64-bit ABCpdf and vice versa. Indeed, a license may be installed successfully without being valid for the current process so it is a good idea to check LicenseValid after installing a system license. For security reasons, you should not use this method unless you have complete control of the system on which you are installing. You need to make this call from an elevated process. |  |  | 
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