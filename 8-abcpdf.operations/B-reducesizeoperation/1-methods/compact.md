---
title: "compact"
css: "abcpdf-docs.css"
---

|  |  | Compact Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Compact and compress the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Compact(bool wholeDocument) ``` [Visual Basic] `Function Compact(wholeDocument As Boolean)` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| wholeDocument | Whether to compact the entire document or only selected pages. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Compact and compress the document. The two main types of resources which take up file space are images and embedded fonts. As such this method allows you to resize images to a lower resolution, compress them using different methods and quality settings and remove embedded fonts. The particular options appropriate to your documents can be set using the properties on this operation. During processing ProcessingObject and ProcessedObject events will be fired for each font or image object that is being operated upon. Using the arguments included with these events you can take finer control over the application of this operation. If you have previously added content to the document it will need to be frozen in place. This may result in changes to the Doc.HtmlOptions, Doc.Rendering and Doc.SaveOptions properties. You may also wish to set the SaveOptions.CompressObects property to true, to further reduce the output size on save. This type of operations is fairly complex and can take some time on larger documents. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following example shows how to compress a document. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); using (var op = new ReduceSizeOperation(doc)) op.Compact(true); doc.Save(Server.MapPath("ReduceSizeOperation.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) Using op As New ReduceSizeOperation(doc) op.Compact(True) End Using doc.Save(Server.MapPath("ReduceSizeOperation.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>