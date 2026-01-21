---
title: "breakzonesize"
css: "abcpdf-docs.css"
---

|  |  | BreakZoneSize Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 75 | No | The percentage of the current drawing area in which HTML breaks can occur. | 

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
      
| The size of drawing area in which page breaks are allowed. When HTML is added to a PDF page, it is placed within the current Doc.Rect. In general, you do not want page breaks to occur too high up in this area. So ABCpdf only scans for good break locations towards the bottom. This property determines how far up (in terms of a percentage) from the bottom that ABCpdf will scan for a good break location. |  |  | 
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