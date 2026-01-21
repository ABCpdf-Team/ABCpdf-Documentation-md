---
title: "validate"
css: "abcpdf-docs.css"
---

|  |  | Validate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Check and validate the status of this signature. |  |  | 

</td>
      </tr>

      <tr>
        <td class="sectheader" valign="top"><img src=
        "../../../images/steel-pin.gif" height="10" width="64">  

        Syntax</td>

        <td width="14">&nbsp;</td>

        <td valign="top">
          
| **[C#]** ```csharp bool Validate() bool Validate(string[] certificatePaths) bool Validate(System.Collections.IEnumerable certificates) bool Validate(Signature.CertificateCollection certificates) // non-caching ``` [Visual Basic] ``` Function Validate() As Boolean Function Validate(certificatePaths() As String) As Boolean Function Validate(certificates As System.Collections.IEnumerable) As Boolean Function Validate(certificates As Signature.CertificateCollection) As Boolean ' non-caching ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</td>
      </tr>

      <tr>
        <td class="sectheader" valign="top"><img src=
        "../../../images/steel-pin.gif" height="10" width="64">  

        Params</td>

        <td width="14">&nbsp;</td>

        <td valign="top">
          
| Name | Description | 
| --- | --- |
| certificatePaths | An array of paths to X.509 certificate (.cer) files. | 
| certificates | An IEnumerable collection of System.Security.Cryptography.X509Certificates.X509Certificate2 objects and string paths; or an Signature.CertificateCollection object | 
| return | True if the certificate is valid. | 

</td>

                <td width="60">&nbsp;</td>

                <td width="11">&nbsp;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>

      <tr>
        <td class="sectheader" valign="top"><img src=
        "../../../images/steel-pin.gif" height="10" width="64">  

        Notes</td>

        <td width="14">&nbsp;</td>

        <td valign="top">
          
| This function returns true if the signature is valid. To be precise, this method updates the properties Algorithm, IsModified, IsTimeValid, IsTrusted and CompliancePades. The return value is true only if the IsModified is false, and all of IsTimeValid, IsSecure and IsTrusted are true. There are two types of signatures. Approval signatures approve a document at a particular point in time. Certification signatures approve the entire document as a one off event. After a document is signed with an approval signature, the document is not necessarily frozen. Most obviously it may need to be updated if another user wishes to add their own signature. Each time the document is updated a new revision is created. The validity of a signature only refers to the revision at which it was signed - the SigningRevision. So while the signing revision does not affect validity you should be careful to take any subsequent revisions into account when reporting back to the user. Similarly there are some subtleties relating to the IsTrusted property which are worth bearing in mind. Hybrid documents may have multiple different visual representations depending on the capabilities of the viewing application, so you may wish to be cautious if your documents contain hybrid sections. For how to detect hybrid sections see the ObjectSoup.Eof.Load method. A document may contain one and only one certification signature. A certification signature applies to the entire document as a whole. You can set permissions to allow small changes to be made after the document is certified and in this case the SigningRevision may not be the last revision. However in general you should be extremely cautious if there are subsequent revisions as it is not easy to determine programatically the importance of the changes that have been made. In this case you may wish to load the document at different revisions and display the rendered content to allow the user to see the changes visually. Signatures' certificates can only be validated by referencing certificates issued by certification authorities. This method allows you to check and validate the status of a signature with reference to a set of such certificates. Additionally, ABCpdf can also use certificates found in the Windows Certificate Store for validation. See ValidationPolicy for details. Except for the non-caching overload, the certificates you provide will be cached at a document level so this function is efficient even when checking multiple signatures within one document. If you do not provide any parameters, this function will use the previously cached certificates to validate the document. Therefore, unless ValidationPolicy is set to EntireChainTrust, or certificates have been provided using a previous call to this function, calling the parameterless overload of this function will cause an exception to be thrown to indicate that there are no certificates to validate against. The overload that takes an Signature.CertificateCollection does not cache the input certificates and does not use any certificates cached with the document. It only uses the certificates provided in the parameter. It allows the use the same set of certificates to validate signatures in multiple documents without re-reading the certificate files. ABCpdf does not do revocation checks on certificates provided and on certificates embedded in a PDF document unless the CompliancePades is set to something other than None. If you need to do this type of operation, you should use the GetCertificates function and check the certificates yourself. If a certificate is unavailable or invalid, this method may throw an exception. This means validating against an unsigned signature field will cause an exception to be thrown. When revocation checking, ABCpdf first checks OCSP responses. If those are not available it will use the CRL. This is the fastest and most effiient way to work. How does Adobe Reader validate a PDF document without certificate files? You may find that Adobe Reader does not need a list of certificate files to validate PDF documents. This is because Adobe Reader may use several built-in Public Key Infrastructure hierarchies to certify PDF documents: Certified Document Services (CDS) is a trust hierarchy that chains back to the Adobe Root Certification Authority (Adobe Root CA). Adobe Approved Trust List (AATL) is an extra list of CA certificates that Adobe Reader may download from Adobe periodically (for Adobe Reader/Acrobat 9 or later). The Windows Certificate Store. This is only true if Windows digital signature integration is enabled in Acrobat, which has not been the default since Acrobat 9. In order to validate a PDF document the same way Adobe Reader does, you need to use the same certificates it uses. This can be easily achieved by exporting the trusted identities from Adobe Reader to .cer format certificate files. (Note: CDS and AATL certificates are usually not in your Windows Certificate Store by default.). These then need to be placed in the Windows Certificate Store. For them to be trusted they need to be in one of the Trusted folder - Trusted People or Trusted Root Certification Authorities. Needless to say, adding items to these folders - particularly the latter - is a big deal and you must be very careful to ensure you know what you are doing. The Windows Certificate Store can be accessed by using System.Security.Cryptography.X509Certificates.X509Store (examples below). | 
| --- |

</td>

                <td width="60">&nbsp;</td>

                <td width="11">&nbsp;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>

      <tr>
        <td class="sectheader" valign="top"><img src=
        "../../../images/steel-pin.gif" height="10" width="64">  
Example</td>

        <td width="14">&nbsp;</td>

        <td valign="top">
          
| [C#] ```csharp // Validate using certificate files using (var doc = new Doc()) { doc.Read(Server.MapPath("../Rez/SignedDocument.pdf")); var theCerts = Server.MapPath("../Rez/JohnSmith.cer").Split(new char[] { ';' }); var theSig = (Signature)doc.Form["Signature"]; if ((theSig.Validate(theCerts)) && (!theSig.IsModified)) doc.AddText($"Signature valid at {DateTime.Now}"); doc.Save(Server.MapPath("SignedAndValidated1.pdf")); } ``` [Visual Basic] ```vbnet ' Validate using certificate files Using doc As New Doc() doc.Read(Server.MapPath("../Rez/Signed.pdf")) Dim theCerts As String() = Server.MapPath("../Rez/JohnSmith.cer").Split(New Char() {";"C}) Dim theSig As Signature = DirectCast(doc.Form("Signature"), Signature) If (theSig.Validate(theCerts)) AndAlso (Not theSig.IsModified) Then doc.AddText($"Signature valid at {DateTime.Now}") End If doc.Save(Server.MapPath("SignedAndValidated1.pdf")) End Using ``` [C#] ```csharp // Validate using the Windows Certificate Store using (var doc = new Doc()) { doc.Read(Server.MapPath("../Rez/SignedDocument.pdf")); var theStore = new X509Store(StoreName.Root, StoreLocation.LocalMachine); theStore.Open(OpenFlags.ReadOnly); var theSig = (Signature)doc.Form["Signature"]; if ((theSig.Validate(theStore.Certificates)) && (!theSig.IsModified)) doc.AddText($"Signature valid at {DateTime.Now}"); theStore.Close(); doc.Save(Server.MapPath("SignedAndValidated2.pdf")); } ``` [Visual Basic] ```vbnet ' Validate using the Windows Certificate Store Using doc As New Doc() doc.Read(Server.MapPath("../Rez/Signed.pdf")) Dim theStore As New X509Store(StoreName.Root, StoreLocation.LocalMachine) theStore.Open(OpenFlags.[ReadOnly]) Dim theSig As Signature = DirectCast(doc.Form("Signature"), Signature) If (theSig.Validate(theStore.Certificates)) AndAlso (Not theSig.IsModified) Then doc.AddText($"Signature valid at {DateTime.Now}") End If theStore.Close() doc.Save(Server.MapPath("SignedAndValidated2.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
      </tr>
    </tbody>
  </table>