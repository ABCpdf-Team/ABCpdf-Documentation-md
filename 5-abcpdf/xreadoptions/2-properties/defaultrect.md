---
title: "defaultrect"
css: "abcpdf-docs.css"
---

|  |  | DefaultRect Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp XRect ``` [Visual Basic]`XRect` | "Letter" | No | The default document size for documents that do not specify a size. | 

</TD><TD width=60>&nbsp;</TD><TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Some document types do not require a document size. For example SVG and PostScript can both be constructed in such a way as to be simply a set of drawing instructions without any details of the size of the output device. Formats like RTF have no default bounding box so always require that one is supplied.This property allows you to specify a default size for use if the document does not specify a size. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>