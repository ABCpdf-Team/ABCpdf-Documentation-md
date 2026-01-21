---
title: "datetimeformat"
css: "abcpdf-docs.css"
---

|  |  | DateTimeFormat Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IFormatProvider ``` [Visual Basic] `IFormatProvider` | null | No | The format provider for formatting dates and times. | 

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
      
| This property specifies the formats of dates and times for the appearances of fields that use javascript functions such as AFDate_FormatEx, AFTime_FormatEx. A null value indicates the use of the locale-independent default formats. You can see the appearances when the PDF is rendered to an image. If the fields are not stamped, Adobe Reader may ignore the appearances and generate new appearances so you may not see the dates and times in the specified formats when viewing in Adobe Reader. |  |  | 
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