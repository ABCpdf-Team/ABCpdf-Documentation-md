---
title: "errors"
css: "abcpdf-docs.css"
---

|  |  | Errors Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp IList ``` [Visual Basic]`IList(Of String)` | null | Yes | The validation errors. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property holds the validation errors. If any errors are emitted, then the document is not compliant. Each PDF/A error indicates the problem and also the part of the specification which is not being adhered to. Some errors indicate problem with the PDF rather than the PDF/A specification. In this case, no specification section is emitted. For example, the following errors might be emitted. ```error Outline item 88's required Count is missing. PDF/A-1 6.3.5 Font subsets: Type-0 font 198 is a font subset without CIDSet. PDF/A-1 6.3.6 Font metrics: TrueType font 201's Widths is inconsistent with the embedded font program. PDF/A-1 6.7.3 Document information dictionary: Metadata 15--Document "Producer" and XMP property pdf:Producer are different. ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Read method. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>