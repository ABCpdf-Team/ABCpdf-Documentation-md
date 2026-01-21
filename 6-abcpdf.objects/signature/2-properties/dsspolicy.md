---
title: "dsspolicy"
css: "abcpdf-docs.css"
---

|  |  | DSSPolicy Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp RevocationPolicy ``` [Visual Basic] `RevocationPolicy` | OcspThenCrl | No | The revocation policy to adopt when checking for the Document Security Store (DSS). | 

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
      
| The revocation policy to adopt when checking for the Document Security Store (DSS). The RevocationPolicy enumeration may take the following values: None - No revocation policy. Ocsp - Use OCSP to check for revocation. Crl - Use CRL to check for revocation. OcspThenCrl - Use OCSP and then CRL to check for revocation. CrlThenOcsp - Use CRL and then OCSP to check for revocation. With the OcspThenCrl and CrlThenOcsp selectors, the first method is used and the responses checked. If they are all valid then the process will go no further and the responses will be embedded in the DSS. If the responses are unavailable or invalid then the second method will be tried instead. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>