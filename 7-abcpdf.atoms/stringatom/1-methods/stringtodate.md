---
title: "stringtodate"
css: "abcpdf-docs.css"
---

|  |  | StringToDate Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Convert a standard PDF date string into a DateTime. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp static string StringToDate(DateTime dateTime) ``` [Visual Basic] `Shared Function StringToDate(dateTime As DateTime) As String` |  |  | 
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
| dateTime | The standard PDF date string. | 
| return | The DateTime to be converted. | 

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
      
| Convert a standard PDF date string into a DateTime. The PDF date string covers date, time and time zone. The format is broadly similar to ASN.1 as detailed in ISO/IEC 8824. For example, February 3, 2017, at 9:14 PM Pacific Standard Time would be represented as "D:201702032114-08'00". |  |  | 
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