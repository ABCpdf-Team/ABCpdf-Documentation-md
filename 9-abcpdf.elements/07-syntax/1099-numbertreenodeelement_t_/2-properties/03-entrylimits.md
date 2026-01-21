---
title: "03-entrylimits"
css: "abcpdf-docs.css"
---

|  |  | EntryLimits Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | This property represents the "Limits" entry of the number tree node dictionary object. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property represents the "Limits" entry of the number tree node dictionary object. It is defined as part of the PDF 1.0 specification. It is an Array containing two integer representing the lower and upper bounds of the tree. The first int represents the lowest key in the EntryNums entry of this or any child nodes. The second int represents the highest key in the EntryNums entry of this or any child nodes. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 37, page 91. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>