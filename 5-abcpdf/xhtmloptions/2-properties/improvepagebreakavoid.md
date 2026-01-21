---
title: "improvepagebreakavoid"
css: "abcpdf-docs.css"
---

|  |  | ImprovePageBreakAvoid Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to improve the support for page-break-inside of avoid. | 

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
      
| The Gecko engine does not support some complex uses of CSS style "page-break-inside:avoid". In particular, it does not work well when this style is applied inside table elements. Set this property to true to improve the layout of elements using this style. |  |  | 
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