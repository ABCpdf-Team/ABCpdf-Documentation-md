---
title: "pinch"
css: "abcpdf-docs.css"
---

|  |  | Pinch Effect |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The Pinch effect distorts the image as if it had been pinched. |  |  | 

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Settings</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Default | Description | 
| --- | --- | --- |
| Amount | 50 % | The amount that the image should be pinched. | 
| Extent | 50 % | How far the effect should extend. | 
| Speed | 3 | There is a general speed versus quality tradeoff. Higher values produce faster results at the expense of quality. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Workings</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The effect distorts the image as if it had been pinched. |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example images show the effect of a Pinch filter applied to a picture with different settings. [C#] ```csharp void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img3); // original image doc.Rendering.Save("EffectPinch.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Pinch")) { effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectPinchDefault.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Pinch")) { effect.Parameters["Amount"].Value = 75; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectPinchAmount75.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Pinch")) { effect.Parameters["Extent"].Value = 100; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectPinchExtent100.jpg"); } } ``` [Visual Basic] ```vbnet Sub ... Using doc As New Doc() AddImagePage(doc, img3) ' original image doc.Rendering.Save("EffectPinch.jpg") Using layer As ImageLayer = AddImagePage(doc, img3) Using effect As New EffectOperation("Pinch") effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectPinchDefault.jpg") Using layer As ImageLayer = AddImagePage(doc, img3) Using effect As New EffectOperation("Pinch") effect.Parameters("Amount").Value = 75 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectPinchAmount75.jpg") Using layer As ImageLayer = AddImagePage(doc, img3) Using effect As New EffectOperation("Pinch") effect.Parameters("Extent").Value = 100 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectPinchExtent100.jpg") End Using End Sub ``` Original Image before Pinch After Pinch with default settings Amount = 75 Extent = 100 |  |  | 
| --- | --- | --- |

    </td>
  </tr>
</table>