---
title: "reason"
css: "abcpdf-docs.css"
---

|  |  | Reason Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | null | No | The reason for signing. | 

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
      
| The reason for signing. If you wish to set a value for this property, you should do so before calling the Sign function. This property can take null as a value. This indicates that no reason was given. Note that this property can only be relied on if the certificate is valid. You can check whether the certificate is valid using the Validate function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the Sign function. Also see example code in: Signature Sign Method, Signature CompliancePades Property, Signature CustomSigner Property, Signature CustomSigner2 Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>