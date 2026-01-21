---
title: "ismodified"
css: "abcpdf-docs.css"
---

|  |  | IsModified Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | Yes | True if the PDF has been tampered with after signing. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </tbody></table>
    </td>
  </tr>
  
  <tr> 
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property allows you to determine if the PDF has been tampered with after signing. It is important to understand that certain types of updates are allowed. The validity of this property relates to the validity of the particular revision of the document. So it allows you to determine if the original PDF has been tampered with in any way. However it is possible to update PDF by incrementally updating the revision. This will provide a document which contains modifications but can be backtracked to show the exact state of the document at the point that a particular signature was applied. Most commonly this is needed when multiple signatures are being applied as each signature needs to be applied to a new revision of the document and to be valid for that particular revision. See also the Validate function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</tbody></table>