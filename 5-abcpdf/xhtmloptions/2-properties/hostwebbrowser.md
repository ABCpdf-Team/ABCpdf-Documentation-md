---
title: "hostwebbrowser"
css: "abcpdf-docs.css"
---

|  |  | HostWebBrowser Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true (overridable by registry value) | No | Whether to host a WebBrowser control. | 

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
      
| This property determines whether a WebBrowser control is hosted. By default, a WebBrowser control is hosted. Script-accessible properties (left, top, width, height, offsetLeft, offsetTop, offsetWidth, offsetHeight, clientLeft, clientTop, clientWidth, clientHeight, pixelLeft, pixelTop, pixelWidth, pixelHeight, posLeft, posTop, posWidth, and posHeight) hold their proper values. The source document can be in any format as long as it is HTML-compatible. For example, XML (with or without XSL applied) can be used because the WebBrowser control transforms it to HTML. When no WebBrowser control is hosted, script-accessible dynamic, geometric properties are always zero. This property affects the CoerceVector property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</tbody></table>