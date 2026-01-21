---
title: "1-certificatecollection"
css: "abcpdf-docs.css"
---

|  |  | CertificateCollection Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| CertificateCollection Constructor. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp CertificateCollection() CertificateCollection(Signature.CertificateCollection certs) CertificateCollection(X509Certificate2 cert) CertificateCollection(X509Certificate2[] certs) ``` [Visual Basic] ``` Sub New Sub New(certs As Signature.CertificateCollection) Sub New(cert As X509Certificate2) Sub New(certs() As X509Certificate2) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| certs | A Signature.CertificateCollection object or an array of System.Security.Cryptography.X509Certificates.X509Certificate2 objects. | 
| cert | A System.Security.Cryptography.X509Certificates.X509Certificate2 object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| These methods construct a Signature.CertificateCollection object. Signature.CertificateCollection does not store duplicate certificates, so only one certificate object among each set of duplicates is included if an array of X509Certificate2 is provided. |  |  | 
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