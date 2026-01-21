---
title: "TimestampHashAlgorithm"
css: "abcpdf-docs.css"
---

|  |  | TimestampHashAlgorithm Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp System.Security.Cryptography.Oid ``` [Visual Basic] `System.Security.Cryptography.Oid` | Oid("SHA256") | No | The hash algorithm used to create the digest for timestamp requests. | 

</td>
<td width="60">&nbsp;</td>
<td>&nbsp;</td>
</tr>
</tbody>
</table>
</td>
</tr>

<tr>
<td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  

Notes</td>
<td width="14">&nbsp;</td>
<td valign="top">

| This property enables you to specify the hash algorithm to be used for timestamp requests using your desired Time Stamping Authority (TSA). In signature workflows there may be a number of different timestamps: The signature itself may be timestamped as with PAdES B_T compliance. An optional timestamp entry (/TS) may be added to the /VRI entry in the Document Security Store (DSS) for PAdES B_LT. A document timestamp is a special form of signature certifying the document at a particular time, as with PAdES B_LTA compliance. For convenience when a signature is created with SignatureCompliance set to a level above PAdES_B_B this value is used to compute the digests for all required timestamping operations. Note that MD5 or SHA1 should not be used where PAdES conformance is required. It is unlikely that you would need to change this from the default Oid for SHA256. |  |  | 
| --- | --- | --- |

</td>
</tr>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR>
</tbody>
</table>