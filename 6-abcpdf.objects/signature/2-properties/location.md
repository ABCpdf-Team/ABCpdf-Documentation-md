---
title: "location"
css: "abcpdf-docs.css"
---

|  |  | Location Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | null | No | The location of the signing. | 

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
      
| The location of the signing. If you wish to set a value for this property, you should do so before calling the Sign function. This property can take null as a value. This indicates that no location was provided. Note that this property can only be relied on if the certificate is valid. You can check whether the certificate is valid using the Validate function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the Sign function. Also see example code in: Signature Sign Method, Signature CompliancePades Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>