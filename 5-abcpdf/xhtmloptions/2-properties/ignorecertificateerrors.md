---
title: "ignorecertificateerrors"
css: "abcpdf-docs.css"
---

|  |  | IgnoreCertificateErrors Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to ignore certificate-related errors. | 

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
      
| This property determines whether certificate-related errors are ignored or not. When retrieving pages via https URLs, ABCpdf will check that the SSL certificate is valid and trusted. If it is not you may not wish to proceed with the HTML render and instead throw an exception. Using this property you can control whether error will be ignored or reported. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
|  |  |  | 
| --- | --- | --- |

</td>
  </tr>
</tbody></table>