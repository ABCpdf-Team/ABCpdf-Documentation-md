---
title: "issecure"
css: "abcpdf-docs.css"
---

|  |  | IsSecure Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | Yes | True if the signature and document look well formed and well applied. | 

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

| True if the signature and document look well formed and well applied. A signature with a PDF document occupies a specific portion of that document and should cover the rest of the document. However it is possible to create signatures which conform technically but are badly or suspiciously applied. For example one could create a signature which did not cover the start of a document. While this is legal it is not sensible and this kind of structure should be regarded as insecure. This property can be used to determine whether the signature has been well and sensibly applied. |  |  | 
| --- | --- | --- |

</td>
</tr>
</tbody>
</table>