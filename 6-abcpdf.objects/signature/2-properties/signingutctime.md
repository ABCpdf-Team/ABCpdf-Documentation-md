---
title: "signingutctime"
css: "abcpdf-docs.css"
---

|  |  | SigningUtcTime Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp DateTime ``` [Visual Basic] `DateTime` | See description. | No | The time of signing in UTC format. | 

`may throw Exception()`

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
      
| The time of signing in UTC format. When you call the Sign function, the UTC time is automatically updated. Note that this property can only be relied on if the certificate is valid. You can check whether the certificate is valid using the Validate function. You will not need to change the value of this property unless you are writing low level signature manipulation code. If the format of the date in the PDF is incorrect, then querying the value of this property may result in an exception being thrown. |  |  | 
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