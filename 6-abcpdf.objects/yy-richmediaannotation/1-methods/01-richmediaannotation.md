---
title: "01-richmediaannotation"
css: "abcpdf-docs.css"
---

|  |  | RichMediaAnnotation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds rich media to the current page of the doc. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp RichMediaAnnotation(Doc doc, XRect rect, string filePathOrUrl, string mediaType) ``` [Visual Basic] ``` RichMediaAnnotation(doc As Doc, rect As XRect, filePathOrUrl As string, mediaType As string) ``` |  |  | 
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
| filePathOrUrl | Media file path or URL | 
| mediaType | Media type | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds rich media to the current page of the doc. The media type can be one of: "Flash" "Video" "Sound" "3D" Supported file formats are not defined by the PDF specification and thus will vary between viewers. |  |  | 
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