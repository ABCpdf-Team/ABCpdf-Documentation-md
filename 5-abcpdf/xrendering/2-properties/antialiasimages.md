---
title: "antialiasimages"
css: "abcpdf-docs.css"
---

|  |  | AntiAliasImages Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to anti-alias images. | 

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
      
| Determines whether image transformations will be interpolated. This feature is most useful when the original embedded image resolution is greater than the output resolution. When this property is set to true interpolation is used to scale images thus increasing output quality. Whether the edges of images are anti-aliased is determined by the AntiAliasPolygons property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows the effect that this parameter has on PDF rendering. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/HyperX.pdf")); doc.Rect.Inset(200, 200); // Render document with AntiAliasImages = true (default) doc.Rendering.Save(Server.MapPath("RenderingAntiAliasImagesTrue.png")); // Render document with AntiAliasImages = false doc.Rendering.AntiAliasImages = false; // Save the image doc.Rendering.Save(Server.MapPath("RenderingAntiAliasImagesFalse.png")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/HyperX.pdf")) doc.Rect.Inset(200, 200) ' Render document with AntiAliasImages = true (default) doc.Rendering.Save(Server.MapPath("RenderingAntiAliasImagesTrue.png")) ' Render document with AntiAliasImages = false doc.Rendering.AntiAliasImages = False ' Save the image doc.Rendering.Save(Server.MapPath("RenderingAntiAliasImagesFalse.png")) End Using ``` RenderingAntiAliasImagesTrue.png RenderingAntiAliasImagesFalse.png |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>