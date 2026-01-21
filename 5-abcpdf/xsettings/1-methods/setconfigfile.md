---
title: "setconfigfile"
css: "abcpdf-docs.css"
---

|  |  | SetConfigFile Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the application configuration using a Linux style config file. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static void SetConfigFile(string path) ``` [Visual Basic] ``` Shared Function SetConfigFile(path As string) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The path to the config file. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Set the application configuration file. This can be used in situations in which you have a custom config file for your application - most commonly on Linux. On Windows ABCpdf first looks for preferences in the default config file. For an executable this will be app.config in the same directory as the executable. For a web site it will be a web.config at the root of the web app. Under Linux this does not happen. If a preference is not found here then any config file specified using the SetConfigFile method will be scanned for an appropriate setting. If the method has not been called and you are on Linux then the default config file will be used - ~/.config/WebSupergoo/ABCpdf13.config. On Windows if the preference is still not found then the registry will be scanned for the value. Finally if no value has been found then a default will be used. Here is an example of a .config file that contains a valid ABCpdf config section. The illustrated ABCpdf preferences are TempDirectory and MakeURLsUnique. ``` ``` Important: must appear before if exists. | 
| --- |

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| For an example of how to specify a confiig sectoin see the SetConfigSection method. None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>