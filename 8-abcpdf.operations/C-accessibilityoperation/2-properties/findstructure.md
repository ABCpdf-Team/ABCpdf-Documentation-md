---
title: "findstructure"
css: "abcpdf-docs.css"
---

|  |  | FindStructure Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to detect and insert structure outline. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Whether to detect and insert structure outline. PDF document structure tags are analogous to header tags in HTML: they allow one to structure document content as a hierarchy. For example a document might be divided first by article then by section then by chapter. There are specific named hierarchy types available but in general an abstract hierarchical structure is all that is required. If this property is set to true, the AccessibilityOperation will attempt to detect document structure and insert appropriate tags to mark it as such. If your documents are complicated and you require complete control over the detection process, you can do this using the techniques detailed in the AccessiblePDF example project which comes with ABCpdf. |  |  | 
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