---
title: "getcertificates"
css: "abcpdf-docs.css"
---

|  |  | GetCertificates Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Extract the encoded X.509 data of the certificate(s). |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IEnumerable GetCertificates() IEnumerable GetCertificates(out int outCount) ``` [Visual Basic] ``` Function GetCertificates() As IEnumerable(Of Byte()) Function GetCertificates( ByRef outCount As Integer) As IEnumerable(Of Byte()) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| outCount | The number of certificates. | 
| return | The encoded X.509 data for the certificate(s). | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to extract the encoded X.509 data of the certificate that was used to sign the document. Normally, there is only one certificate returned, but for some documents, you may receive additional certificates that can be used to create a certificate chain. In such cases, the first certificate is always the certificate that was used for signing. You can pass the data returned by this function to the X509Certificate2 class constructor in System.Security.Cryptography.X509Certificates and then extract certificate details such as the subject, the issuer, the serial number, the version, etc. See the Annotations example project for details. |  |  | 
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