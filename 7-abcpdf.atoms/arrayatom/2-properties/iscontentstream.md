---
title: "iscontentstream"
css: "abcpdf-docs.css"
---

|  |  | IsContentStream Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Determines whether the ArrayAtom represents a content stream or not. | 

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
      
| Determines whether the ArrayAtom represents a content stream or not. ArrayAtoms do not normally contain streams or operators. To allow them to do this you need to set this property to true. In most situations ABCpdf will parse the content stream for you and set the property appropriately. However if you creating your own streams you may need to specify that the array needs to support these types of atoms. |  |  | 
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