---
title: "indexof"
css: "abcpdf-docs.css"
---

|  |  | IndexOf Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the index of the certificate object's value. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int IndexOf(X509Certificate2 cert) ``` [Visual Basic]`Function IndexOf(cert As X509Certificate2) As Integer` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| cert | The certificate object. | 
| return | The index of the certificate object or of its value in this collection if found; -1 otherwise. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method returns the index of the certificate object's value. Because of the no-duplicate policy of Signature.CertificateCollection, it is not recommended to remove certificate objects to undo a previous addition to the collection unless you are sure that the certificate object has been successfully added at that particular addition. You may want to consider using the copy constructor to make a copy of the collection, instead, before doing the addition. |  |  | 
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