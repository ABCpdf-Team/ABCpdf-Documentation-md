---
title: "addnames"
css: "abcpdf-docs.css"
---

|  |  | AddNames Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` ? [Visual Basic] `Boolean?` | null | No | Whether HTML name attributes should be tracked. | 

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

| Whether HTML name attributes should be tracked. The benefit of tracking these attributes is that they allow internal links to be resolved when calling LinkPages. The disadvantage of tracking is that there may be many such attributes and this can represent a processing overhead. The default value of null allows the effective value to be determined by the HTML engine. Currently only the ABCChrome85 engine supports this property. |  |  | 
| --- | --- | --- |

</td>
</tr>
<tr>
<td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  

Example</td>
<td width="14">&nbsp;</td>
<td valign="top">

| None. |  |  | 
| --- | --- | --- |

</td>
</tr>
</tbody>
</table>