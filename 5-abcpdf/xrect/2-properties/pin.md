---
title: "pin"
css: "abcpdf-docs.css"
---

|  |  | Pin Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Corner ``` [Visual Basic] `Corner` | Corner.BottomLeft | No | The corner of the rectangle to pin. | 

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
      
| Allows you change the pinned corner of the rectangle. The Corner enumeration may take the following values: BottomLeft TopLeft BottomRight TopRight Some operations require that the rectangle is pinned to a location. For example if you want to change the width of a rectangle you can do this either by shifting the left side or the right side. If the pin property is set to the bottom or top left then the left side of the rectangle will be kept fixed and the right side shifted. Conversely if the pin property is set to the bottom or top right then the right side of the rectangle will be kept fixed and the left side shifted. Why is my Pin a number? In older versions of ABCpdf the Pin property was a number. To assign a Corner to the Pin property you needed to cast the value. So you might find code of this form. [C#] ```csharp theRect.Pin = (int)XRect.Corner.TopRight; ``` [Visual Basic] ```vbnet theRect.Pin = CInt(XRect.Corner.TopRight) ``` In Version 8 the Pin property has been changed to a true enumeration. This means you can assign the Corner directly. [C#] ```csharp theRect.Pin = XRect.Corner.TopRight; ``` [Visual Basic] ```vbnet theRect.Pin = XRect.Corner.TopRight ``` If your code is bound to integers rather than enumerations then it is safe to cast the number to a Corner. [C#] ```csharp theRect.Pin = (XRect.Corner)myIntegerValue; ``` [Visual Basic] ```vbnet theRect.Pin = CType(myIntegerValue, XRect.Corner) ``` | 
| --- |

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: ABCpdf eForm Placeholder Example, Doc TopDown Property, XRendering DrawAnnotations Property, Page GetBitmap Function, PixMap SetAlpha Function, PixMap ToGrayscale Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>