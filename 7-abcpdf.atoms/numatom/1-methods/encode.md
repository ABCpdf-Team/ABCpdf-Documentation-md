---
title: "encode"
css: "abcpdf-docs.css"
---

|  |  | Encode Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Encode a number into a PDF string. This format may be needed for direct insertion into a content stream. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp static string Encode(double value) ``` [Visual Basic] `Shared Function Encode(value As Double) As String` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| value | The number to convert. | 
| return | The string representation. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Encode a number into a PDF string. This format may be needed for direct insertion into a content stream. PDF content streams accept certain formats of numbers. In many situations these are the same as the strings returned by .NET functions such as ToString. However in the case of floating point conversions, not all output formats are valid in a PDF content stream. For example, very small or very large numbers can lead to the insertion of exponential format strings which are not an accepted PDF format and can lead to errors. Because numbers typically occur in a non exponential range these errors can be infrequent and difficult to track down. This method will produce PDF valid strings for use in content streams and similar applications. |  |  | 
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