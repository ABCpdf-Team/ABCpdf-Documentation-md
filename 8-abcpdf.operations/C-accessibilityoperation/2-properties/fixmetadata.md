---
title: "fixmetadata"
css: "abcpdf-docs.css"
---

|  |  | FixMetadata Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to attempt to fix or add metadata that may be required for accessibility. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Whether to attempt to fix or add metadata that may be required for accessibility. Specifications like PDF/UA mandate certain requirements. One of the core requirements is that XMP metadata is embedded in the document. This property controls whether an attempt will be made to add any such data. Information for the XMP section will be extracted from the info section of the PDF. A PDF/UA tag will be added as will other required features like a title. |  |  | 
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