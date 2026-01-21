---
title: "conformance"
css: "abcpdf-docs.css"
---

|  |  | Conformance Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp PdfConformance ``` [Visual Basic]`PdfConformance` | Pdf | No | The PDF conformance. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property specifies the conformance for validation. It can take any of the following values: Pdf – PDF conformance. PdfA1b - PDF/A Part 1 Level B conformance. PdfA1a - PDF/A Part 1 Level A conformance. PdfA2b - PDF/A Part 2 Level B conformance. PdfA2u - PDF/A Part 2 Level U conformance. PdfA2a - PDF/A Part 2 Level A conformance. PdfA3b - PDF/A Part 3 Level B conformance. PdfA3u - PDF/A Part 3 Level U conformance. PdfA3a - PDF/A Part 3 Level A conformance. In general you will be wanting to validate against PdfA1b, PdfA2b or PdfA3b - PdfA3b is the parent standard of PdfA3u and PdfA3a. ABCpdf cannot validate against PdfA2a or PdfA3a because the standard includes features which can only be determined by humans. For example it requires that images of text be tagged with the text that is displayed in the image. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Read method. Also see example code in: PdfValidationOperation Read Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>