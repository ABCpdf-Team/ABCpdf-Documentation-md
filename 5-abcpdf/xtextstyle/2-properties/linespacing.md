---
title: "linespacing"
css: "abcpdf-docs.css"
---

|  |  | LineSpacing Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 0.0 | No | The inter-line spacing. | 

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
      
| Allows you to adjust the distance between lines of text. At the start of every new line of text, the text drawing position is shifted vertically by the distance specified in this property. If the value is positive this will space the lines out. If the value is negative it will shift the lines together. You can use the following code to adopt the linespacing from an embedded font. [C#] ```csharp FontObject font = (FontObject)doc.ObjectSoup[doc.Font]; doc.TextStyle.LineSpacing = (font.FontLineSpacing * doc.TextStyle.Size) / 1000; ``` [Visual Basic] ```vbnet Dim font As FontObject = CType(doc.ObjectSoup(doc.Font), FontObject) doc.TextStyle.LineSpacing = (font.FontLineSpacing * doc.TextStyle.Size) / 1000 ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In the following example we add three blocks of text to a document. The first block uses the default line spacing. The second block uses a positive value to space out the lines. The last block uses a negative value to shift the lines together. [C#] ```csharp using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani..."; doc.TextStyle.Size = 48; doc.AddText(text); doc.Rect.Move(0, -250); doc.TextStyle.LineSpacing = 20; doc.AddText(text); doc.Rect.Move(0, -350); doc.TextStyle.LineSpacing = -20; doc.AddText(text); doc.Save(Server.MapPath("stylelspace.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani..." doc.TextStyle.Size = 48 doc.AddText(theText) doc.Rect.Move(0, -250) doc.TextStyle.LineSpacing = 20 doc.AddText(theText) doc.Rect.Move(0, -350) doc.TextStyle.LineSpacing = -20 doc.AddText(theText) doc.Save(Server.MapPath("stylelspace.pdf")) End Using ``` stylelspace.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>