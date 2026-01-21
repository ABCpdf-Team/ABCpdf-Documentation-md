---
title: "hpos"
css: "abcpdf-docs.css"
---

|  |  | HPos Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 0? | No? | The current horizontal positioning factor (0 to 1). | 

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
      
| This property determines the horizontal offset of blocks of text - used for left alignment, right alignment or centering. The offset is measured as a proportion of the distance from the left. A value of zero indicates left alignment, a value of one half indicates centered text and a value of one indicates right alignment. Intermediate values can be used for intermediate offsets. To vertically align text use the VPos property. To justify text use the Justification property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code adds two blocks of text to a document. The first block is left aligned and the second is right aligned. Before adding the text we change the current rectangle and frame it so that you can see how the text is aligned. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; doc.Rect.Magnify(1.0, 0.5); doc.Rect.Inset(40, 40); doc.FrameRect(); doc.AddText("Left justified text..."); doc.Rect.Move(0, doc.Rect.Height + 80); doc.FrameRect(); doc.TextStyle.HPos = 1.0; doc.AddText("Right justified text..."); doc.Save(Server.MapPath("dochpos.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 doc.Rect.Magnify(1.0, 0.5) doc.Rect.Inset(40, 40) doc.FrameRect() doc.AddText("Left justified text...") doc.Rect.Move(0, doc.Rect.Height + 80) doc.FrameRect() doc.TextStyle.HPos = 1.0 doc.AddText("Right justified text...") doc.Save(Server.MapPath("dochpos.pdf")) End Using ``` dochpos.pdf Also see example code in: ABCpdf Deletion Example, ABCpdf Headers and Footers Example, Doc AddPage Function, Doc Append Function, Doc Read Function, Doc RemapPages Method, XRendering SaveAlpha Property, XTransform AngleUnit�Property, XpsImportOperation Import Function, SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>