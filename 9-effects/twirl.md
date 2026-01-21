---
title: "twirl"
css: "abcpdf-docs.css"
---

|  |  | Twirl Effect |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The Twirl effect distorts the image as if it had been twirled. |  |  | 

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Settings</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Default | Description | 
| --- | --- | --- |
| Angle | 120 degrees | The amount that the image should be twirled. | 
| Extent | 50 % | How far the effect should extend. | 
| Speed | 8 | There is a general speed versus quality tradeoff. Higher values produce faster results at the expense of quality. | 

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
      
| The effect distorts the image as if it had been twisted. |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following examples show the effect of a Twirl applied with a number of different settings. [C#] ```csharp void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img3); // original image doc.Rendering.Save("EffectTwirl.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Twirl")) { effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectTwirlDefault.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Twirl")) { effect.Parameters["Angle"].Value = 360; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectTwirlAngle360.jpg"); using (ImageLayer layer = AddImagePage(doc, img3)) { using (EffectOperation effect = new EffectOperation("Twirl")) { effect.Parameters["Extent"].Value = 100; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectTwirlExtent100.jpg"); } } ``` [Visual Basic] ```vbnet Sub ... Using doc As New Doc() AddImagePage(doc, img3) ' original image doc.Rendering.Save("EffectTwirl.jpg") Using layer As ImageLayer = AddImagePage(doc, img3) Using effect As New EffectOperation("Twirl") effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectTwirlDefault.jpg") Using layer As ImageLayer = AddImagePage(doc, img3) Using effect As New EffectOperation("Twirl") effect.Parameters("Angle").Value = 360 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectTwirlAngle360.jpg") Using layer As ImageLayer = AddImagePage(doc, img3) Using effect As New EffectOperation("Twirl") effect.Parameters("Extent").Value = 100 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectTwirlExtent100.jpg") End Using End Sub ``` Original Image before Twirl After Twirl with default settings Angle = 360 Extent = 100 |  |  | 
| --- | --- | --- |

    </td>
  </tr>
</table>