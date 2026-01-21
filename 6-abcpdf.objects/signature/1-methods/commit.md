---
title: "commit"
css: "abcpdf-docs.css"
---

|  |  | Commit Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Commit a previously signed signature to the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Commit() ``` [Visual Basic]`Sub Commit()` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| none |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| After a signature is signed, it needs to be committed to the document. Normally, this is done when you save the document. It happens invisibly without you needing to do anything. However, sometimes, you may wish to commit before the document is saved. This most commonly occurs if you are working with documents containing more than one signature field. The PDF architecture requires that a document be incrementally updated each time a signature is signed. It requires this so that a PDF viewer can show what changes were made to the document between the times it was signed. For this reason, if you are signing multiple fields, each signature (bar the last) needs to be signed and then committed in turn. The last signature does not need to be committed because this is implicitly done by the final save. A Commit operation involves an implicit Doc.Save event. For this reason it is important that the Doc.SaveOptions are appropriately set up before the signature is Committed. If you intending to commit to a document containing multiple signatures you will want to ensure that the XSaveOptions.Incremental property is set. Similarly after each commit, all previous references to form fields are invalidated. You need to obtain updated references to form fields from the Doc.Form.Fields property. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: Signature AddLTV Function, Signature CustomSigner2 Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>