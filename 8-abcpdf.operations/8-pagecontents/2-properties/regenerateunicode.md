---
title: "regenerateunicode"
css: "abcpdf-docs.css"
---

|  |  | RegenerateUnicode Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to attempt to regenerate missing Unicode tables from embedded fonts. | 

`may throw Exception()`

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Whether to attempt to regenerate missing Unicode tables from embedded fonts. For details of the type of fix that is attempted on non-conforming fonts please see the FontObject.RegenerateToUnicode method. This property must not be changed after the AddPages method has been called. To do so will result in an exception being raised. |  |  | 
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