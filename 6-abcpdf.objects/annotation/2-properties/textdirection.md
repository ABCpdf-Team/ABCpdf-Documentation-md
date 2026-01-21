---
title: "textdirection"
css: "abcpdf-docs.css"
---

|  |  | TextDirection Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XTextStyle.DirectionType ``` [Visual Basic] `XTextStyle.DirectionType` | DirectionType.Default | No | The default text direction | 

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
      
| This property specifies the default primary text direction. For the details of each value, please refer to XTextStyle.Direction. The value of this property is not saved to the PDF file and it exists purely to determine the way that appearances are generated for annotations containing text. If you are using Hebrew or Arabic you may wish to set this value to left-to-right to provide support to bi-directional text and contextual ligatures. In general you will not want to set the primary direction to right-to-left as this is something that Acrobat does not support and may result in field changes when, in Acrobat, you click into a field to edit the text. |  |  | 
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