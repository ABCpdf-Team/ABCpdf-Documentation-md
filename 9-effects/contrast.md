---
title: "contrast"
css: "abcpdf-docs.css"
---

|  |  | Contrast Effect |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The Contrast effect can be used to increase or decrease the contrast of an image. |  |  | 

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Settings</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Default | Description | 
| --- | --- | --- |
| Amount | 0 % | Amount to increase or decrease contrast by. | 

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
      
| The value given is used to stretch the contrast within the image. Values greater than zero increase the amount of contrast while those less than zero decrease the contrast. |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following show the effect of increasing and decreasing contrast. [C#] ```csharp void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img2); // original image doc.Rendering.Save("EffectContrast.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Contrast")) { effect.Parameters["Amount"].Value = 25; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectContrast25.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Contrast")) { effect.Parameters["Amount"].Value = 50; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectContrast50.jpg"); using (ImageLayer layer = AddImagePage(doc, img2)) { using (EffectOperation effect = new EffectOperation("Contrast")) { effect.Parameters["Amount"].Value = -50; effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectContrast-50.jpg"); } } ``` [Visual Basic] ```vbnet Sub ... Using doc As New Doc() AddImagePage(doc, img2) ' original image doc.Rendering.Save("EffectContrast.jpg") Using layer As ImageLayer = AddImagePage(doc, img2) Using effect As New EffectOperation("Contrast") effect.Parameters("Amount").Value = 25 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectContrast25.jpg") Using layer As ImageLayer = AddImagePage(doc, img2) Using effect As New EffectOperation("Contrast") effect.Parameters("Amount").Value = 50 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectContrast50.jpg") Using layer As ImageLayer = AddImagePage(doc, img2) Using effect As New EffectOperation("Contrast") effect.Parameters("Amount").Value = -50 effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectContrast-50.jpg") End Using End Sub ``` Original Image | Contrast Amount 25 | 
| --- | --- |
| Contrast Amount 50 | Contrast Amount -50 | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>    </td>
  </tr>
</table>