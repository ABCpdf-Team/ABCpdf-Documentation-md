---
title: "addresource"
css: "abcpdf-docs.css"
---

|  |  | AddResource Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add a particular type of resource |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string AddResource(IndirectObject resource, string type, string name) ``` [Visual Basic] ``` Function AddResource(resource As IndirectObject, type As String, name As String) As String ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| resource | The resource to be added. | 
| type | The type of resource. | 
| name | The format of the name that should be used. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add a particular type of resource to the Form XObject. Form XObjects may contain default resources usable by the page content stream. The most common resource types are "Font", "XObject" and "ColorSpace". For further details see the PDF Specification. This method allows you to add new resources to the Form XObject. You may supply your own name for the resource but if the name is already in use, it may need to be modified. For this reason the function returns the value which was actually used for the addition. |  |  | 
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