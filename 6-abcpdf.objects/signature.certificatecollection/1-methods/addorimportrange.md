---
title: "addorimportrange"
css: "abcpdf-docs.css"
---

|  |  | AddOrImportRange Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds the certificate objects or imports the certificates from the files to this collection for those whose values are not already present. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddOrImportRange(IEnumerable cert) ``` [Visual Basic]`Function AddOrImportRange(cert As IEnumerable) As Integer` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| certs | A System.Collections.IEnumerable of (System.Security.Cryptography.X509Certificates.X509Certificate2) certificate objects and (string) file paths. | 
| return | The number of certificate objects added. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method adds the certificate objects to the collection for those whose values are not already present. Each item in certs must be either an X509Certificate2 object or a string. Signature.CertificateCollection does not store duplicate certificates, so only one certificate object among each set of duplicates is added. |  |  | 
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