---
title: "1-introduction"
css: "abcpdf-docs.css"
---

|  |  | Introduction to Effects |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Effects are an operation which can be applied to images. They include common and useful functions like blur and sharpen filters. |  |  | 

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Basics</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Effects are applied using the EffectOperation class. To apply an effect you can use code as simple as this. [C#] ```csharp void function() { using (Doc doc = new Doc()) { AddImagePage(doc, img5); using (ImageLayer layer = AddImagePage(doc, img5)) { using (EffectOperation effect = new EffectOperation("Sharpen")) { effect.Apply(layer.PixMap); } } doc.Rendering.Save("EffectSharpen1b.jpg"); } ``` [Visual Basic] ```vbnet Sub ... Using doc As New Doc() AddImagePage(doc, img5) Using layer As ImageLayer = AddImagePage(doc, img5) Using effect As New EffectOperation("Sharpen") effect.Apply(layer.PixMap) End Using End Using doc.Rendering.Save("EffectSharpen1b.jpg") End Sub ``` |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Examples</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The examples make use of a function named AddImagePage. This function simply creates an appropriate Doc object, adds the image and returns the ImageLayer which was added. [C#] ```csharp private ImageLayer AddImagePage(Doc doc, string path) { using (XImage img = XImage.FromFile(path, null)) { doc.MediaBox.SetSides(0, 0, img.Width, img.Height); doc.Page = doc.AddPage(); doc.Rect.String = doc.MediaBox.String; int id = doc.AddImageObject(img); return (ImageLayer)doc.ObjectSoup[id]; } } ``` [Visual Basic] ```vbnet Private Function AddImagePage(doc As Doc, path As String) As ImageLayer Using img As XImage = XImage.FromFile(path, Nothing) doc.MediaBox.SetSides(0, 0, img.Width, img.Height) doc.Page = doc.AddPage() doc.Rect.[String] = doc.MediaBox.[String] Dim id As Integer = doc.AddImageObject(img) Return DirectCast(doc.ObjectSoup(id), ImageLayer) End Using End Function ``` |  |  | 
| --- | --- | --- |

    </td>
  </tr>
</table>