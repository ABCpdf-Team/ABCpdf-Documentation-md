---
title: "fileextension"
css: "abcpdf-docs.css"
---

|  |  | FileExtension Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic]`String` | null | No | Gets or sets the file extension for data sources that do not have file names. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property is used by modules that can take files with different file extensions when (and only when) the specification of the source does not provide a file extension, such as a Stream or an array of bytes. For the Default modules, it is optional, but the modules may behave differently when it is specified. For the XpsAny and the OpenOffice modules, it is mandatory. |  |  | 
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