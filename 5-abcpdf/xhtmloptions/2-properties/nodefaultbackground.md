---
title: "nodefaultbackground"
css: "abcpdf-docs.css"
---

|  |  | NoDefaultBackground Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to disable the default background color. | 

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
      
| When the HTML page does not specify a background color, the Gecko engine applies the default background color specified by preference browser.display.background_color or overridden by preference browser.display.use_system_colors. This default color is always opaque. Because the default preference specifies white, you get a white background (which you likely do not notice unless there is already some objects on the PDF page) if this property is set to false. |  |  | 
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