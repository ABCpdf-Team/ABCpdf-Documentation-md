---
title: "encryption"
css: "abcpdf-docs.css"
---

|  |  | Encryption Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp XEncryption ``` [Visual Basic] `XEncryption` | No encryption. | No | The current encryption settings. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property determines the current encryption settings. When you save the document the encryption settings - if any - will be used to determine the method of encryption to be used. By default documents are not encrypted when created. However if you read an existing PDF document the encryption property will be updated to reflect the encryption settings used to create the original document. PDF encryption supports two different types of password - a user password and an owner password. You can use either password to open and view the document. However unless you supply the owner password, permissions will be applied and access to the document may be restricted. Typically PDF encryption is used to apply permissions to a document. The user password is left blank and only an owner password supplied. PDF readers will not prompt for a password if there is no user password. However any permissions will automatically be applied. In this way you can allow anyone to open the document but restrict access to operations like copying text, printing the document or extracting images. The PDF 2.0 standard deprecates a number of these options as being potentially insecure. The recommended set for PDF 2.0 compliant documents is XEncryption.Type 5 with XEncryption.SetCryptMethods AESV3. Please note that you are legally bound to respect the permissions present in existing PDF documents. For details please see the Legal Requirement Section. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code saves a simple PDF document using a 128 bit encryption key. It applies a copy-protection permission to stop people copying text out of the document. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; doc.AddText("Hello World!"); doc.Encryption.Type = 5; doc.Encryption.SetCryptMethods(CryptMethodType.AESV3); doc.Encryption.CanCopy = false; doc.Encryption.OwnerPassword = "owner"; doc.Save(Server.MapPath("docencrypt.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 doc.AddText("Hello World!") doc.Encryption.Type = 5 doc.Encryption.SetCryptMethods(CryptMethodType.AESV3) doc.Encryption.CanCopy = False doc.Encryption.OwnerPassword = "owner" doc.Save(Server.MapPath("docencrypt.pdf")) End Using ``` Also see example code in: XEncryption SetCryptMethods Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>