---
title: "useproxyserver"
css: "abcpdf-docs.css"
---

|  |  | UseProxyServer Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to use a proxy server. | 

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
      
| This property determines whether to use a proxy server. The process of detecting and using a proxy server involves an overhead that is usually not necessary. For this reason, by default, we do not use proxy server settings. Setting this property to true will mean that ABCpdf will detect and use proxy server settings. Transitioning between proxy and non-proxy settings also involves an overhead. So it is best to keep this value constant for all calls to AddImageUrl or AddImageHtml. |  |  | 
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