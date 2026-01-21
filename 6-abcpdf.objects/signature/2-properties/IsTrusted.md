---
title: "IsTrusted"
css: "abcpdf-docs.css"
---

|  |  | IsTrusted Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | Yes | True if the signature's certificate is trusted according to the validation policy. | 

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

Example</td>
<td width="14">&nbsp;</td>
<td valign="top">

| See the Validate function and the ValidationPolicy property for details of how this property is determined. Note that it is possible for a signature to be untrusted but still PAdES compliant. For example if a document was signed a decade ago it might no longer be possible to validate the trust chain so it would be untrusted. However PAdES Long Term Validation (LTV) signatures embedded in the document might provide evidence that the signature had been compliant. If those the LTV signatures are trusted, by impllcation the signature itself is still trusted. This type of situation is indicated by an IsTrusted value of false and a ComplaincePades which is not None. |  |  | 
| --- | --- | --- |

</td>
</tr>
</tbody>
</table>