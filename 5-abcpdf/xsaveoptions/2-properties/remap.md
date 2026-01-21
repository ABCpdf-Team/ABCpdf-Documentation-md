---
title: "remap"
css: "abcpdf-docs.css"
---

|  |  | Remap Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to reduce size by remapping objects. | 

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
      
| This property determines if output size should be reduced by remapping objects. PDF documents consist of a sequence of numbered objects. If objects have been deleted there may be gaps in this sequence. Gaps can lead to PDFs which are larger than necessary. If this property is set to true then, when the document is saved, remapping will occur to eliminate these gaps. Note that if the Linearize property is set to true then remapping will occur no matter the value of this property. |  |  | 
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