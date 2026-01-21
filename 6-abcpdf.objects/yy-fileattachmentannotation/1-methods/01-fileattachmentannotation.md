---
title: "01-fileattachmentannotation"
css: "abcpdf-docs.css"
---

|  |  | FileAttachmentAnnotation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add file attachment annotation to the current page of the doc. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp FileAttachmentAnnotation(Doc doc, XRect rect, string filePath) FileAttachmentAnnotation(Doc doc, XRect rect, byte[] data, string fileName, DateTime modDate, DateTime creationDate) ``` [Visual Basic] ``` FileAttachmentAnnotation(doc As Doc, rect As XRect, filePath As string) FileAttachmentAnnotation(doc As Doc, rect As XRect, data() As Byte, fileName As string, modDate As DateTime, creationDate As DateTime) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | Doc | 
| rect | Annotation rectangle | 
| filePath | File path | 
| data | The data from a file to be embedded | 
| fileName | The name of the file to be embedded | 
| modDate | The file modification date | 
| creationDate | The file creation date | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add file attachment annotation to the current page of the doc. |  |  | 
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