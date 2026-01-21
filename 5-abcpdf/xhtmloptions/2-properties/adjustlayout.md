---
title: "adjustlayout"
css: "abcpdf-docs.css"
---

|  |  | AdjustLayout Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether HTML layout is checked and adjusted for optimal output to PDF. | 

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
      
| This property determines whether HTML layout is checked and adjusted for optimal output to PDF. HTML layout is optimized for screen based output on a scrolling display. Certain types of percentage based sizing can give rise to situations in which the proportions of the different elements do not add up to 100%. On screen this type of confused layout is less noticable than it is on a paged medium like PDF. When set the document is scanned for typical layout based errors and these are fixed. However if you are not using these features then skipping the adjustment stage can save time with no noticable change in output quality. |  |  | 
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