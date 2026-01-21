---
title: "certify"
css: "abcpdf-docs.css"
---

|  |  | Certify Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Make this a certification signature. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Certify() void Certify(PermittedChanges changes) ``` [Visual Basic] ``` Sub Certify() Sub Certify(changes As PermittedChanges) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| changes | The document changes which will be permitted after the signature is signed. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Make this a certification signature. A document may contain at most one certification signature. A certification signature applies to the entire document as a whole and is used to determine document level integrity. Typically a certification signature is used by the author of a document to freeze the document and specify in what ways it may be modified. Then, if the author has allowed it, other people may apply approval signatures to the frozen document. The PermittedChanges enumeration may take the following values: None - No changes are permitted. FormFilling - Form filling is permitted. Annotations - Form filling and annotation addition is permitted. |  |  | 
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