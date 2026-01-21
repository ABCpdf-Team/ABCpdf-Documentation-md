---
title: "tograyscale"
css: "abcpdf-docs.css"
---

|  |  | ToGrayscale Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Converts the image to grayscale. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void ToGrayscale() ``` [Visual Basic] ``` Sub ToGrayscale() ``` |  |  | 
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
| none |  | 

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
      
| This allows you to convert an image to grayscale. It can be useful for preparing soft masks. This function is a convenience method for this common operation. A practically identical effect can be achieved using the Recolor method followed by Compress. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Here we add an image in its natural color space and then, at a position down and to the right, converted to grayscale. [C#] ```csharp using var doc = new Doc(); doc.Rect.Pin = XRect.Corner.TopLeft; doc.Rect.Magnify(0.5, 0.5); string path = Server.MapPath("../mypics/mypic.jpg"); doc.AddImageFile(path, 1); doc.Rect.Move(doc.Rect.Width, -doc.Rect.Height); int i = doc.AddImageFile(path, 1); var im = (ImageLayer)doc.ObjectSoup[i]; im.PixMap.ToGrayscale(); doc.Save(Server.MapPath("pixmaptograyscale.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Pin = XRect.Corner.TopLeft doc.Rect.Magnify(0.5, 0.5) Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") doc.AddImageFile(thePath, 1) doc.Rect.Move(doc.Rect.Width, -doc.Rect.Height) Dim i As Integer = doc.AddImageFile(thePath, 1) Dim im As ImageLayer = DirectCast(doc.ObjectSoup(i), ImageLayer) im.PixMap.ToGrayscale() doc.Save(Server.MapPath("pixmaptograyscale.pdf")) End Using ``` pixmaptograyscale.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>