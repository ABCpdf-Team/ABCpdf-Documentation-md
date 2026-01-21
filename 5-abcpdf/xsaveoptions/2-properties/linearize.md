---
title: "linearize"
css: "abcpdf-docs.css"
---

|  |  | Linearize Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to linearize the output for fast web viewing. | 

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
      
| This property determines if output should be linearized for fast viewing over the web. Linearized PDFs are organized in a special way to enable efficient access over the web. The output is valid PDF in all ways but it is structured to allow web viewers to access only the portions of the PDF that they need. From a practical point of view this means that a Linearized PDF opens instantly rather than requiring that the entire PDF is downloaded before it can be seen. Adobe sometimes refer to Linearization as Fast Web View. There is a performance and memory overhead associated with linearization. However this is something that you should normally only notice when handling huge documents. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: FileSpecification FileSpecification Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>