---
title: "antialiastext"
css: "abcpdf-docs.css"
---

|  |  | AntiAliasText Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to anti-alias text. | 

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
      
| Determines whether text will be rendered with anti-aliased edges. Anti-aliasing is a technique for using gradients of color to eliminate jagged edges when objects are drawn. The object edges are blurred to reduce pixelation. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows the effect that this parameter has on PDF rendering. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(50, 50); // Add some text doc.FontSize = 48; doc.Pos.String = "50 690"; int id = doc.AddText("Abc"); // Render images doc.Rect.String = doc.GetInfo(id, "rect"); doc.Rendering.AntiAliasText = true; using var antialiasedBitmap = doc.Rendering.GetBitmap(); doc.Rendering.AntiAliasText = false; using var aliasedBitmap = doc.Rendering.GetBitmap(); // Add enlarged images to the pdf file doc.Rect.Magnify(5, 5); doc.Rect.Move(0, -300); doc.AddImageBitmap(aliasedBitmap, false); doc.Rect.Move(0, -300); doc.AddImageBitmap(antialiasedBitmap, false); // Annotate doc.Rect.String = doc.MediaBox.String; doc.Color.String = "255 0 0"; doc.FontSize = 36; doc.Pos.String = "50 740"; doc.AddText("Original text:"); doc.Pos.String = "50 620"; doc.AddText("Magnified aliased image:"); doc.Pos.String = "50 320"; doc.AddText("Magnified antialiased image:"); // Save render of pdf files doc.Rendering.AntiAliasText = true; doc.Rendering.DotsPerInch = 36; doc.Rendering.Save(Server.MapPath("RenderingAntiAliasText.png")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(50, 50) ' Add some text doc.FontSize = 48 doc.Pos.String = "50 690" Dim id As Integer = doc.AddText("Abc") ' Render images doc.Rect.String = doc.GetInfo(id, "rect") doc.Rendering.AntiAliasText = True Dim antialiasedBitmap As Bitmap = doc.Rendering.GetBitmap() doc.Rendering.AntiAliasText = False Dim aliasedBitmap As Bitmap = doc.Rendering.GetBitmap() ' Add enlarged images to the pdf file doc.Rect.Magnify(5, 5) doc.Rect.Move(0, -300) doc.AddImageBitmap(aliasedBitmap, False) doc.Rect.Move(0, -300) doc.AddImageBitmap(antialiasedBitmap, False) ' Annotate doc.Rect.String = doc.MediaBox.[String] doc.Color.String = "255 0 0" doc.FontSize = 36 doc.Pos.String = "50 740" doc.AddText("Original text:") doc.Pos.String = "50 620" doc.AddText("Magnified aliased image:") doc.Pos.String = "50 320" doc.AddText("Magnified antialiased image:") ' Save render of pdf files doc.Rendering.AntiAliasText = True doc.Rendering.DotsPerInch = 36 doc.Rendering.Save(Server.MapPath("RenderingAntiAliasText.png")) End Using ``` RenderingAntiAliasText.png |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>