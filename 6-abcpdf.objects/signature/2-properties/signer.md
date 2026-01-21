---
title: "signer"
css: "abcpdf-docs.css"
---

|  |  | Signer Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | See description. | No | The name of the person signing. | 

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
      
| The name of the person signing. When you call the Sign function the name of the signer is automatically updated to match the name associated with the private key. Note that this property can only be relied on if the certificate is valid. You can check whether the certificate is valid using the Validate function. You will not need to change the value of this property unless you are writing low level signature manipulation code. |  |  | 
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