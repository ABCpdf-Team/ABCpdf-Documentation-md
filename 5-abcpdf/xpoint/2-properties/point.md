---
title: "point"
css: "abcpdf-docs.css"
---

|  |  | Point Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Point ``` [Visual Basic] `Point` | n/a | No | The System.Drawing.Point. | 

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
      
| The point as a System.Drawing Point. Windows coordinates are measured in distances from the top left of the drawing surface while PDF coordinates are measured from the bottom left. So when you use this property the coordinates must be re-mapped. This needs to be done in the context of a containing object. Properties such as the Doc.Pos are interpreted in the context of the Doc.MediaBox. If there is no containing object then no re-mapping can be performed. You may find it easier to work with .NET Points than PDF points. However remember that operations such as Transforms work on the underlying PDF coordinates and not on the abstracted Windows coordinates. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code adds three words to a document. The positioning is done using standard .NET Points. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; Point pt = doc.Pos.Point; pt.Offset(100, 150); doc.Pos.Point = pt; doc.AddText("One"); pt.Offset(100, 150); doc.Pos.Point = pt; doc.AddText("Two"); pt.Offset(100, 150); doc.Pos.Point = pt; doc.AddText("Three"); doc.Save(Server.MapPath("xptpt.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 Dim pt As Point = doc.Pos.Point pt.Offset(100, 150) doc.Pos.Point = pt doc.AddText("One") pt.Offset(100, 150) doc.Pos.Point = pt doc.AddText("Two") pt.Offset(100, 150) doc.Pos.Point = pt doc.AddText("Three") doc.Save(Server.MapPath("xptpt.pdf")) End Using ``` xptpt.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>