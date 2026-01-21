---
title: "media"
css: "abcpdf-docs.css"
---

|  |  | Media Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp MediaType ``` [Visual Basic] ``` MediaType ``` | Print | No | The CSS media type to use. | 

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
      
| The MediaType enumeration can take any of the following values: PrintScreen For the Gecko engine, the Screen media must be used with UseScript true. An invalid combination (i.e. Screen with UseScript false) yields an exception when you call AddImageUrl or AddImageHtml. The same HTML document can achieve different visual representations when rendered on different media by specifying several sets of CSS styles for each medium type. The Gecko engine supports the rendering of Web pages using the print stylesheets and the screen stylesheets. When the Screen media is used in conjunction with the Gecko engine, ABCpdf obtains and stores the web page locally before invoking the engine. Since ABCpdf does not obtain additional headers from the Gecko engine, they are not sent in the request. The kind of headers that may not be sent include Accept, Accept-Language, Accept-Encoding, Keep-Alive, and Accept-Charset. The User-Agent may be different. In most situations, this is unimportant, but if you are relying on these headers, you can use the HtmlOptions.HttpAdditionalHeaders property to add your own headers to the request. |  |  | 
| --- | --- | --- |

</td>
  </tr>
    <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: ABCpdf Paged HTML Example. |  |  | 
| --- | --- | --- |

</TD></TR>
</tbody></table>