---
title: "setchromakey"
css: "abcpdf-docs.css"
---

|  |  | SetChromakey Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets a chromakey transparent color for this image. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void SetChromakey(string chromakey) ``` [Visual Basic] ``` Sub SetChromakey(chromakey As String) ``` |  |  | 
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
| chromakey | A chromakey string to assign to this image. | 

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
      
| This allows you to assign a transparent color or color range to the image. You need to specify two values for each component of the color. For a particular pixel, if all the components of the color fall within the specified ranges, then the pixel will not be displayed. For example, to make pure white elements of an RGB transparent you might specify, [C#] ```csharp doc.SetChromakey("255 255 255 255 255 255"); ``` [Visual Basic] ```vbnet doc.SetChromakey("255 255 255 255 255 255") ``` If you wanted to include colors which were off-white you might use, [C#] ```csharp doc.SetChromakey("250 255 250 255 250 255"); ``` [Visual Basic] ```vbnet doc.SetChromakey("250 255 250 255 250 255") ``` This function is equivalent to setting the PixMap "/Mask" entry to an array of color values. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Here we add an image over the top of a green background. We use a chromakey to make black and near-black colors transparent. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(20, 20); doc.Color.String = "0 255 0"; doc.FillRect(); string path = Server.MapPath("../mypics/mypic.jpg"); int i = doc.AddImageFile(path, 1); var im = (ImageLayer)doc.ObjectSoup[i]; im.PixMap.SetChromakey("0 50 0 50 0 50"); doc.Save(Server.MapPath("pixmapsetchromakey.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(20, 20) doc.Color.String = "0 255 0" doc.FillRect() Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") Dim i As Integer = doc.AddImageFile(thePath, 1) Dim im As ImageLayer = DirectCast(doc.ObjectSoup(i), ImageLayer) im.PixMap.SetChromakey("0 50 0 50 0 50") doc.Save(Server.MapPath("pixmapsetchromakey.pdf")) End Using ``` pixmapsetchromakey.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>