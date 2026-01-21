---
title: "pagecacheenabled"
css: "abcpdf-docs.css"
---

|  |  | PageCacheEnabled Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether the page cache should be searched before rendering the page. | 

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
      
| ABCpdf holds a cache of recently requested URLs, and it's only after five minutes or so that these pages expire from the cache. Searching the page cache before rendering a URL results in a considerable degree of optimization for many common operations. However, if you wish to bypass the cache, you can do so by setting this property to false. When the cache is disabled, the registry value MakeURLsUnique takes effect, and the actual URL may be modified. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: XHtmlOptions UseScript Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>