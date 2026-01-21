---
title: "addltv"
css: "abcpdf-docs.css"
---

|  |  | AddLTV Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add Long Term Validation (LTV) to the Document Security Store (DSS). |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void AddLTV(Oid oid) ``` [Visual Basic] `Overridable Sub AddLTV(oid As Oid)` ``` may throw Exception() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| oid | The hash algorithm to use to create the digest of the signature to be timestamped where uri is specified, for example new Oid("SHA256"). | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add Long Term Validation (LTV) to the Document Security Store (DSS). The signature must have been signed and committed prior to calling this method. The certificate used to sign the signature must be time-valid at the time of the call or an exception will be thrown. The signing certificate and any other certificates in the signing certificate's chain of trust are extracted from the signature. Additional reference certificates may be added to the ReferenceCertificates member of this Signature. Each of these certificates is added to the document as a stream, along with any Online Certificate Status Protocol(OCSP) responses and/or Certificate Revocation Lists (CRLs) obtained. The DSS dictionary is created containing references to these streams. In addition a signature Validation Related Information (VRI) entry is added which enables fast lookup of information from the DSS. If the TimestampServiceUrl is set an RFC 3161 timestamp will be stored as a stream with its reference set in to the VRI TS entry. It it is null then the VRI TU value will be set to the current time from the computer's clock. For more information see ISO 32000-2:2017 Section 12.8.4 (https://www.iso.org/standard/63534.html). |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| In this example, for simplicity, we use the plain text password overload. However to improve application security you may wish to use the SecureString overload. [C#] ```csharp using var doc = new Doc(); X509Certificate2 cert = Certificates.GetFromStore(); // User-defined function if (cert == null) return; // no certificate found doc.Page = doc.AddPage(); var sig = doc.Form.AddSignature(new XRect("340 160 540 220"), "Signature"); sig.Sign(cert, false); sig.Commit(); sig = (Signature)doc.Form.Fields["Signature"]; sig.TimestampServiceUrl = new Uri("http://timestamp.comodoca.com"); sig.AddLTV(new Oid(CryptoConfig.MapNameToOID("SHA256"))); doc.Save(Server.MapPath("SignedLTV.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim cert As New X509Certificate2(Server.MapPath("MyCertificate.p12"), "mypassword", X509KeyStorageFlags.Exportable) doc.Page = doc.AddPage() Dim sig As Signature = doc.Form.AddSignature(New XRect("340 160 540 220"), "Signature") sig.Sign(cert, False) sig.Commit() sig = DirectCast(doc.Form.Fields("Signature"), Signature) sig.TimestampServiceUrl = New Uri("http://timestamp.comodoca.com") sig.AddLTV(New Oid(CryptoConfig.MapNameToOID("SHA256"))) doc.Save(Server.MapPath("SignedLTV.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>