---
title: "timeout"
css: "abcpdf-docs.css"
---

|  |  | Timeout Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 20,000 | No | The maximum amount of time allowed for obtaining a page (ms). | 

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
      
| HTML rendering can take some time. If the time taken exceeds the Timeout then the page is assumed to be unavailable. Depending on the RetryCount settings the page may be re-requested or an error may be returned. This value is measured in milliseconds. For cases in which you have the HTML you do not really need a retry so you can set the RetryCount to zero. If you do not do this the default is five. So if your HTML takes 350 seconds to process and your Timeout is 300 seconds then it will time out six times before returning. You allow five minutes but you actually take thirty and still fail to load the HTML because each try does not have enough time. |  |  | 
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