---
title: "paraspacing"
css: "abcpdf-docs.css"
---

|  |  | ParaSpacing Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 0.0 | No | The inter-paragraph spacing. | 

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
      
| Allows you to adjust the distance between paragraphs. At the start of every new paragraph the text drawing position is shifted vertically by the distance specified in this property. If the value is positive this will space the paragraphs out. If the value is negative it will shift the paragraphs together. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we add two blocks of text to a document. The first block uses the default paragraph spacing. The second block uses a positive value to space out the paragraphs. [C#] ```csharp using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes lingua, institutis, legibus inter se differunt."; text = text + "\r\n" + text + "\r\n" + text + "\r\n" + text; doc.Rect.Inset(20, 40); doc.TextStyle.Size = 16; doc.AddText(text); doc.Rect.Move(0, -350); doc.TextStyle.ParaSpacing = 20; doc.AddText(text); doc.Save(Server.MapPath("stylepspace.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes lingua, institutis, legibus inter se differunt." theText = theText + vbCr & vbLf + theText + vbCr & vbLf + theText + vbCr & vbLf + theText doc.Rect.Inset(20, 40) doc.TextStyle.Size = 16 doc.AddText(theText) doc.Rect.Move(0, -350) doc.TextStyle.ParaSpacing = 20 doc.AddText(theText) doc.Save(Server.MapPath("stylepspace.pdf")) End Using ``` stylepspace.pdf Also see example code in: Doc TextStyle Property, XTextStyle Indent Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>