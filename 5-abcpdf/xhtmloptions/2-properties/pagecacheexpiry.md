---
title: "pagecacheexpiry"
css: "abcpdf-docs.css"
---

|  |  | PageCacheExpiry Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 300,000 | No | The length of time that pages can be held in the cache (ms). | 

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
      
| ABCpdf holds a cache of recently requested URLs and it's only after five minutes or so that these pages expire from the cache. This results in a considerable degree of optimization for many common operations. You can modify the length of time that pages are held in the cache using this parameter. This value cannot be reduced to zero. This value is measured in milliseconds. |  |  | 
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