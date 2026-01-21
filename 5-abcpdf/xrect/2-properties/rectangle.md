---
title: "rectangle"
css: "abcpdf-docs.css"
---

|  |  | Rectangle Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Rectangle ``` [Visual Basic] `Rectangle` | n/a | No | The System.Drawing.Rectangle. | 

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
      
| The rectangle as a System.Drawing Rectangle. Windows coordinates are measured in distances from the top left of the drawing surface while PDF coordinates are measured from the bottom left. So when you use this property the coordinates must be re-mapped. This needs to be done in the context of a containing object. Properties such as the Doc.Rect and the XImage.Selection have containers but others such as the Doc.MediaBox do not. In these cases the rectangles are assumed to contain themselves. You may find it easier to work with .NET Rectangles than PDF rectangles. However remember that operations such as Transforms work on the underlying PDF coordinates and not on the abstracted Windows coordinates. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code adds two blocks of text to a document. The positioning is done using standard .NET Rectangles. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; var rc = doc.MediaBox.Rectangle; rc.Inflate(-50, -50); rc.Height = 250; doc.Rect.Rectangle = rc; doc.FrameRect(); doc.AddText("First Rectangle..."); rc.Offset(0, 300); doc.Rect.Rectangle = rc; doc.FrameRect(); doc.AddText("Second Rectangle..."); doc.Save(Server.MapPath("xrectrectangle.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 Dim rc As Rectangle = doc.MediaBox.Rectangle rc.Inflate(-50, -50) rc.Height = 250 doc.Rect.Rectangle = rc doc.FrameRect() doc.AddText("First Rectangle...") rc.Offset(0, 300) doc.Rect.Rectangle = rc doc.FrameRect() doc.AddText("Second Rectangle...") doc.Save(Server.MapPath("xrectrectangle.pdf")) End Using ``` xrectrectangle.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>