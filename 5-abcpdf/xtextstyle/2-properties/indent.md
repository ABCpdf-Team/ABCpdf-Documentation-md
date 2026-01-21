---
title: "indent"
css: "abcpdf-docs.css"
---

|  |  | Indent Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 0 | No | The first line of paragraph indent. | 

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
      
| This property determines the horizontal indent applied to the first line of every paragraph. If the indent is positive the start of the first line is shifted to the right by the specified number of points. If the indent is negative it is shifted to the left by the specified number of units. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we add a block of text to a document. We specify a ParaSpacing value to space out the paragraphs and an Indent value to indent the first line of each paragraph. [C#] ```csharp using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes lingua, institutis, legibus inter se differunt."; text = text + text; text = text + "\r\n" + text + "\r\n"; text = text + text + text + text; doc.Rect.Inset(20, 40); doc.TextStyle.Size = 16; doc.TextStyle.ParaSpacing = 16; doc.TextStyle.Indent = 48; doc.AddText(text); doc.Save(Server.MapPath("styleindent.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes lingua, institutis, legibus inter se differunt." theText = theText + theText theText = theText + vbCr & vbLf + theText + vbCr & vbLf theText = theText + theText + theText + theText doc.Rect.Inset(20, 40) doc.TextStyle.Size = 16 doc.TextStyle.ParaSpacing = 16 doc.TextStyle.Indent = 48 doc.AddText(theText) doc.Save(Server.MapPath("styleindent.pdf")) End Using ``` styleindent.pdf Also see example code in: Doc TextStyle Property, XTransform Rotate Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>