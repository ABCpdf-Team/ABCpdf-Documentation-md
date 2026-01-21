---
title: "string"
css: "abcpdf-docs.css"
---

|  |  | String Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | Variable | No | A string representation of the graphic style of the document | 

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
      
| A string representation of the graphic style of the document. This covers the Transform, ColorSpace, Color, Font, TextStyle, Width and Options properties. However it does not cover the Page, Layer, Rect or Pos properties. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we show how to use the String property to implement a graphics state stack with Push and Pop operators. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 64; doc.Rect.Inset(20, 20); doc.Font = doc.AddFont("Helvetica"); var state = new Stack(); state.Push(doc.String); doc.AddText("Black Helvetica\r\n\r\n"); doc.Color.SetRgb(255, 0, 0); doc.Font = doc.AddFont("Helvetica-Oblique"); doc.AddText("Red Helvetica-Oblique\r\n\r\n"); doc.String = state.Pop(); doc.AddText("Black Helvetica again\r\n\r\n"); doc.Save(Server.MapPath("savestate.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 64 doc.Rect.Inset(20, 20) doc.Font = doc.AddFont("Helvetica") Dim state As New Stack(Of String)() state.Push(doc.String) doc.AddText("Black Helvetica" & vbCr & vbLf & vbCr & vbLf) doc.Color.SetRgb(255, 0, 0) doc.Font = doc.AddFont("Helvetica-Oblique") doc.AddText("Red Helvetica-Oblique" & vbCr & vbLf & vbCr & vbLf) doc.String = state.Pop() doc.AddText("Black Helvetica again" & vbCr & vbLf & vbCr & vbLf) doc.Save(Server.MapPath("savestate.pdf")) End Using ``` savestate.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>