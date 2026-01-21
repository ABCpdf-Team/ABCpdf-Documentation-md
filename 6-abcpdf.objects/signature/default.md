---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | Signature Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Represents a digital signature field in a document. As well as providing authorization, digital signatures can also be used to detect whether a file has been altered since signing took place. ``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.Field WebSupergoo.ABCpdf13.Objects.Signature ``` |  |  | 

</td>
      </tr>
      <tr>
        <td valign="top">&nbsp;</td>
        <td width="14">&nbsp;</td>
        <td valign="top">
          
| Method | Description | 
| --- | --- |
| Equals | Test whether the two Signatures are the same. | 
| AddLTV | Add Long Term Validation (LTV) to the Document Security Store (DSS). | 
| Certify | Make this a certification signature. | 
| Commit | Commit a previously signed signature to the document. | 
| GetCertificates | Extract the encoded X.509 data of the certificate(s). | 
| LockFields | Lock document fields to stop them being modified. | 
| Sign | Sign the digital signature using a private key and password. | 
| Timestamp | Sign a document timestamp signature field using a Timestamping Authority (TSA). | 
| Validate | Check and validate the status of this signature. | 

</td>
                <td width="60">&nbsp;</td>
                <td width="11">&nbsp;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td valign="top">&nbsp;</td>
        <td width="14">&nbsp;</td>
        <td valign="top">
          
| Property | Description | 
| --- | --- |
| Algorithm | The type of hash algorithm used in the signature. | 
| IsCertification | Whether this a certification signature rather than an approval signature. | 
| IsModified | True if the PDF has been tampered with after signing. | 
| IsSecure | True if the signature and document look well formed and well applied. | 
| IsTrusted | True if the signature's certificate is trusted according to the validation policy. | 
| IsTimeValid | True if the signature's certificate was time-valid when the document was signed. | 
| CompliancePades | The signature compliance level. | 
| CustomSigner | A delegate called to perform custom signing of the PDF. | 
| CustomSigner2 | A delegate called to perform custom signing and timestamping of the PDF. | 
| CustomSignerArgumentType | The type of data to be passed to any custom signer. | 
| DSSPolicy | The revocation policy to adopt when checking for the Document Security Store (DSS). | 
| MaxSignatureLength | Indicates the maximum length of the signature CMS in bytes. | 
| Location | The location of the signing. | 
| Reason | The reason for signing. | 
| Signer | The name of the person signing. | 
| SigningRevision | The revision at which the signature was signed. | 
| SigningUtcTime | The time of signing in UTC format. | 
| TimestampHashAlgorithm | The hash algorithm used to create the digest for timestamp requests. | 
| TimestampServiceUrl | The URL to a time-stamping service. | 
| ReferenceCertificates | Reference certificates for PADES_B_LT and PADES_B_LTA. | 
| ValidationPolicy | The validation policy for certificates. | 
| Validity | The validity of the signature. | 

</td>
                <td width="60">&nbsp;</td>
                <td width="11">&nbsp;</td>
              </tr>
              <tr>
                <td>&nbsp;</td>
                <td width="60">&nbsp;</td>
                <td width="11">&nbsp;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
    </tbody>
  </table>