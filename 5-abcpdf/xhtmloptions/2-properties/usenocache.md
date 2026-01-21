---
title: "usenocache"
css: "abcpdf-docs.css"
---

|  |  | UseNoCache Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether any proxy servers should re-request items of content. | 

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
      
| This property determines whether no-cache is enabled. Setting this property to true forces any intervening proxy server to re-request the page. For the MSHTML engine, setting this property to true sets INTERNET_FLAG_PRAGMA_NOCACHE. WinINET will add request header Pragma: no-cache if going through a HTTP/1.0 proxy and request header Cache-Control: no-cache if going through a HTTP/1.1 proxy. For the Gecko engine, setting this property to true sets the following flags. LOAD_FLAGS_IS_REFRESH — the load should have the semantics of an HTML Meta-refresh tag (i.e., that the cache should be bypassed). LOAD_FLAGS_BYPASS_HISTORY — history should not be updated. LOAD_FLAGS_BYPASS_CACHE — the local web cache should be bypassed (but an intermediate proxy cache could still be used to satisfy the load). LOAD_FLAGS_BYPASS_PROXY — any intermediate proxy caches should be bypassed (i.e., that the content should be loaded from the origin server). |  |  | 
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