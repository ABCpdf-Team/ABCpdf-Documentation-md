---
title: "pageloadmethod"
css: "abcpdf-docs.css"
---

|  |  | PageLoadMethod Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp PageLoadMethodType ``` [Visual Basic] `PageLoadMethodType` | Default | No | The method for loading URI/HTML. | 

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
      
| This property specifies the method to load the URI/HTML page. The PageLoadMethodType enumeration can take any of the following values: Default — this is currently the same as MonikerForHtml. MonikerForHtml — Moniker is used to load the page. WebBrowserNavigate — IWebBrowser2::Navigate is used to load the page. HostWebBrowser must be true to use this value. This property affects the NoCookie property and the GetHttpStatusCode method. |  |  | 
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