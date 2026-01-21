---
title: "1-poolhasstarted"
css: "abcpdf-docs.css"
---

|  |  | PoolHasStarted Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | n/a | Yes | Whether the process pool for the HTML Engine has started. | 

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
      
| This gets whether the process pool for the HTML Engine has started. The process options are used only at the start of the process pool. If the process pool has started, the options are ignored. You can stop the process pool by calling XHtmlOptions.EndTasks so that all worker processes are terminated. |  |  | 
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