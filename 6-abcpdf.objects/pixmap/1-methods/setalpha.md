---
title: "setalpha"
css: "abcpdf-docs.css"
---

|  |  | SetAlpha Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets a constant alpha value (0-255) for this image. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void SetAlpha(double alpha) ``` [Visual Basic] ``` Sub SetAlpha(alpha As Double) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| alpha | A constant alpha value to assign to this image. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Assigns a constant alpha transparency to the PixMap. The alpha value should range from 0 (fully transparent) to 255 (fully opaque). Any values outside this range will result in the alpha channel being removed. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Here we add an image without transparency and then, at a position down and to the right, with 50% transparency. [C#] ```csharp using var doc = new Doc(); doc.Rect.Pin = XRect.Corner.TopLeft; doc.Rect.Magnify(0.5, 0.5); string path = Server.MapPath("../mypics/mypic.jpg"); doc.AddImageFile(path, 1); doc.Rect.Move(doc.Rect.Width, -doc.Rect.Height); int i = doc.AddImageFile(path, 1); var im = (ImageLayer)doc.ObjectSoup[i]; im.PixMap.SetAlpha(128); doc.Save(Server.MapPath("pixmapsetalpha.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Pin = XRect.Corner.TopLeft doc.Rect.Magnify(0.5, 0.5) Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") doc.AddImageFile(thePath, 1) doc.Rect.Move(doc.Rect.Width, -doc.Rect.Height) Dim i As Integer = doc.AddImageFile(thePath, 1) Dim im As ImageLayer = DirectCast(doc.ObjectSoup(i), ImageLayer) im.PixMap.SetAlpha(128) doc.Save(Server.MapPath("pixmapsetalpha.pdf")) End Using ``` pixmapsetalpha.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>