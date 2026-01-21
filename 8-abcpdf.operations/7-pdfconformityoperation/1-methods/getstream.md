---
title: "getstream"
css: "abcpdf-docs.css"
---

|  |  | GetStream Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the conforming document as raw data stream. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Stream GetStream(Doc doc) ``` [Visual Basic]`Function GetStream(doc As Doc) As Stream` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | The document. | 
| return | The PDF document as a stream. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The method writes the document in a conforming PDF format according to the Conformance property. Any conformance error is reported in the Errors property after the method finishes. Because of the CLR limit of 2 GB per object, the GetData method cannot return the data for a document larger than 2 GB. Use this method for documents larger than 2 GB. Dispose of the returned stream as soon as it is no longer needed for small memory footprint. |  |  | 
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