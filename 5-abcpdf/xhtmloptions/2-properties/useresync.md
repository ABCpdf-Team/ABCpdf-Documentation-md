---
title: "useresync"
css: "abcpdf-docs.css"
---

|  |  | UseResync Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to resynchronize pages. | 

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
      
| This property determines whether resync is enabled. When a page is resynchronized, the server is requested to send the new version of the page on the condition that the page in the engine's cache is stale. Setting this property to true sets INTERNET_FLAG_RESYNCHRONIZE. WinINET will send an If-Modified-Since or If-None-Match request header to allow a 304 response, and it may add a request header, as UseNoCache does, to help ensure that an intermediary (proxy) does not return a previously cached result. |  |  | 
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