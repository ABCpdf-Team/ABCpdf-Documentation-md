---
title: "nocookie"
css: "abcpdf-docs.css"
---

|  |  | NoCookie Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to disable automatic cookies. | 

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
      
| This property determines whether automatic cookies are disabled. If it is true, PageLoadMethod must be effectively MonikerForHtml. The HTML engine manages cookies as it receives HTTP/HTTPS responses and sends HTTP/HTTPS requests. If this property is set to true, cookies stored in the local cookie database will not be sent in requests, and cookies received in responses will not be stored in the local cookie database. Cookies specified in HttpAdditionalHeaders are not sent in requests if automatic cookies are enabled. Set this property to true if cookies are specified in HttpAdditionalHeaders. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr>
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| See the HttpAdditionalHeaders property. Also see example code in: XHtmlOptions HttpAdditionalHeaders Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>