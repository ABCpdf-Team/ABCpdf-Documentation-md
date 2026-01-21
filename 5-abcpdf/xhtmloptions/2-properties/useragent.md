---
title: "useragent"
css: "abcpdf-docs.css"
---

|  |  | UserAgent Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "" | No | The user-agent string. | 

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
      
| This property determines the user-agent string for the MSHTML engine. If it is empty, a default user-agent string for Internet Explorer (version 8 or below, depending on the version of Internet Explorer) is used. This is used for downloading the web page as well as all linked resources, whereas User-Agent set in HttpAdditionalHeaders is used only for downloading the web page. If User-Agent is also set in HttpAdditionalHeaders, the HTTP header takes precedence (for downloading the web page). |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
|  |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>