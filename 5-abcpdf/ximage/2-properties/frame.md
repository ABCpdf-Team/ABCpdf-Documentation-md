---
title: "frame"
css: "abcpdf-docs.css"
---

|  |  | Frame Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 1 | No | The currently selected frame. | 

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
      
| Some file formats can contain more than one image. The FrameCount property reflects the number of images. You can change the currently selected image using the Frame property. As you change the frame the Width, Height, HRes and VRes properties will change to reflect the dimensions and resolution of the currently selected image. When you add an Image using the Doc.AddImageObject method the currently selected frame is added. Flash (SWF) movies contain a number of frames. You can set the current frame using this property. If you set this property to a negative number it indicates the number of milliseconds (rather than frames) into the movie. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Here we open a TIFF file using the XImage object. We then scan through each of the images within the file and insert them into a new page of our PDF document. [C#] ```csharp using var img = new XImage(); using var doc = new Doc(); img.SetFile(Server.MapPath("../mypics/multipage.tif")); for (int i = 1; i [Visual Basic] ```vbnet Dim theImg As New XImage() Dim doc As New Doc() theImg.SetFile(Server.MapPath("../mypics/multipage.tif")) Dim i As Integer = 1 While i imageframe.pdf - [Page 1] imageframe.pdf - [Page 2] |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>