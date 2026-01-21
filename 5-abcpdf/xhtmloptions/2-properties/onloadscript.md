---
title: "onloadscript"
css: "abcpdf-docs.css"
---

|  |  | OnLoadScript Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "" | No | A script to be run after the page is loaded. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </tbody></table>
    </td>
  </tr>
  <tr> 
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| A client side JavaScript to be applied to a web page before the page is rendered to PDF. This kind of script can be used for a variety of purposes. For example you might wish to hide background images or get pre-render information from the document. You can provide a return value by setting an "abcpdf" property in the documentElement. For example: [C#] ```csharp document.documentElement.abcpdf = "my return value"; ``` [Visual Basic] ```vbnet document.documentElement.abcpdf = "my return value" ``` The return value can be accessed using the GetScriptReturn method with the ID returned from Doc.AddImageUrl or Doc.AddImageHtml. For the MSHtml engine, you must have the UseScript key set to true or you will get an "access denied" error; the return value can only be set inside OnLoadScript. The Gecko engine does not have these restrictions. For the MSHtml engine, the script in this property is executed after the page load is complete, so it may be executed before or after any script in the web page that is executed after the completion of page load. For the Gecko engine, the script in this property may be executed before or after any event-triggered script in the web page. For example, if you set window.ABCpdf_go to false in OnLoadScript, but the event listener that sets window.ABCpdf_go to true is in the script in the web page, you should check the value of window.ABCpdf_go (initially undefined) before setting it to false in OnLoadScript. [C#] ```csharp doc.HtmlOptions.OnLoadScript = "if(!window.ABCpdf_go) window.ABCpdf_go = false;"; ``` [Visual Basic] ```vbnet doc.HtmlOptions.OnLoadScript = "if(!window.ABCpdf_go) window.ABCpdf_go = false;" ``` For the ABCChrome engine, the script is run at the point that the page and all resources that are referred to by the page, are loaded. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the UseScript property. Also see example code in: XHtmlOptions UseScript Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</tbody></table>