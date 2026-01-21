---
title: "fieldbordercolor"
css: "abcpdf-docs.css"
---

|  |  | FieldBorderColor Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XColor ``` [Visual Basic] `XColor` | n/a | No | The border color of the field. | 

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
      
| This property is used to access or change the border color of a field. This property is only valid if this annotation is associated with a form field. If you assign a color to this property the color supplied must be grayscale, RGB or CMYK. A value of null indicates that the border is transparent. When you set this property a clone of the XColor you assign is created to avoid one XColor being shared by multiple annotations. After changing this property you will need to call UpdateAppearance to realize the change. |  |  | 
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