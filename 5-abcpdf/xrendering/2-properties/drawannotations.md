---
title: "drawannotations"
css: "abcpdf-docs.css"
---

|  |  | DrawAnnotations Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to render fields and annotations. | 

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
      
| Determines whether fields and annotations will be rendered. PDF fields and annotations are not part of the PDF content. Instead they float over the PDF background. You may choose to render these fields or you may wish to avoid rendering them. The export of file types like XPS, DOCX and HTML is implemented using rendering. For this reason the DrawAnnotations proprety will determine if Annotations are exported when saving these formats using the Doc.Save method. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows the effect that this parameter has on PDF rendering. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/Annotations.pdf")); doc.Rect.Pin = XRect.Corner.TopLeft; doc.Rect.Height = 300; // Render document with DrawAnnotations (default) doc.Rendering.Save(Server.MapPath("RenderingDrawAnnotationsTrue.png")); // Render document without DrawAnnotations doc.Rendering.DrawAnnotations = false; doc.Rendering.Save(Server.MapPath("RenderingDrawAnnotationsFalse.png")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/Annotations.pdf")) doc.Rect.Pin = XRect.Corner.TopLeft doc.Rect.Height = 300 ' Render document with DrawAnnotations (default) doc.Rendering.Save(Server.MapPath("RenderingDrawAnnotationsTrue.png")) ' Render document without DrawAnnotations doc.Rendering.DrawAnnotations = False doc.Rendering.Save(Server.MapPath("RenderingDrawAnnotationsFalse.png")) End Using ``` RenderingDrawAnnotationsTrue.png RenderingDrawAnnotationsFalse.png |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>