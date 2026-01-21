---
title: "savequality"
css: "abcpdf-docs.css"
---

|  |  | SaveQuality Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 75 | No | The output file quality for lossy compression. | 

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
      
| This property determines the quality of the output image. It can take values between 0 and 100 ranging from lowest to highest quality. This property is used for JPEG and JPEG 2000 output only. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows the effect that this parameter has on PDF rendering. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/SpaceShuttlePage6.pdf")); doc.Rendering.DotsPerInch = 36; // Save at low quality doc.Rendering.SaveQuality = 5; doc.Rendering.Save(Server.MapPath("RenderingQuality5.jpg")); // Save at high quality doc.Rendering.SaveQuality = 75; doc.Rendering.Save(Server.MapPath("RenderingQuality75.jpg")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/SpaceShuttlePage6.pdf")) doc.Rendering.DotsPerInch = 36 ' Save at low quality doc.Rendering.SaveQuality = 5 doc.Rendering.Save(Server.MapPath("RenderingQuality5.jpg")) ' Save at high quality doc.Rendering.SaveQuality = 75 doc.Rendering.Save(Server.MapPath("RenderingQuality75.jpg")) End Using ``` RenderingQuality5.jpg [file size 9.26 KB] RenderingQuality75.jpg [file size 37.3 KB] |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>