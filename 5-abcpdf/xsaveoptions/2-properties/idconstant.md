---
title: "idconstant"
css: "abcpdf-docs.css"
---

|  |  | IDConstant Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to assign a constant file version identifier. | 

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
      
| This property determines if the file identifiers should be constant rather than unique. PDF documents have two unique file identifiers. One is a file specific identifier which stays constant throughout the life of the file. The other is a file version identifier which is updated every time the document is saved. This property allows you to ensure that the same identifiers are always used. This can be useful for debugging if you need to do a binary level comparison of files and you need to ensure that random elements have been eliminated. |  |  | 
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