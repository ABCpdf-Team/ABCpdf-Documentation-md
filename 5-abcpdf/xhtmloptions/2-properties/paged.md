---
title: "paged"
css: "abcpdf-docs.css"
---

|  |  | Paged Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether content should be rendered in multipaged format. | 

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
      
| This property determines whether HTML should be prepared in a way that allows it to be paged over multiple PDF pages. If paged mode is used then only the first page of the document is drawn. Subsequent pages can be drawn using the Doc.AddImageToChain method. There are subtle differences between paged and non-paged HTML. In general you will want to set this parameter to true even if you only wish to draw one page. |  |  | 
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