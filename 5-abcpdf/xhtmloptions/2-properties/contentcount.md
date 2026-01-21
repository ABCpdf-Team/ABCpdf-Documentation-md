---
title: "contentcount"
css: "abcpdf-docs.css"
---

|  |  | ContentCount Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 50 | No | The minimum number of content items required for a page to be valid. | 

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
      
| The minimum number of items a page of HTML should contain. If the number for the MSHTML engine is less than this value, then the page will be assumed to be invalid For the Gecko engine the content may include non drawing operations such as transforms and state saves and restores. It is only if all items are non-drawing and the total content count is below this value that the page is assumed to be invalid. Typically this will only occur if the system is running low on free memory. Depending on the RetryCount setting (for MSHTML) or the ProcessOptions.RetryCount setting (for Gecko), the page may be re-requested or an error may be returned. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the RetryCount property. Also see example code in: XHtmlOptions RetryCount Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>