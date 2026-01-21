---
title: "italic"
css: "abcpdf-docs.css"
---

|  |  | Italic Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to apply a synthetic italic effect. | 

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
      
| This property determines whether a synthetic italic effect is applied to text. It is generally better to specify an italic typeface rather than synthesize an italic effect using the current typeface. However, under some circumstances this may not be possible and you may prefer to apply a synthetic italic effect. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we add some italic text to a document. [C#] ```csharp using var doc = new Doc(); string text; text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur."; doc.Rect.Inset(20, 40); doc.TextStyle.Size = 96; doc.TextStyle.Italic = true; doc.AddText(text); doc.Save(Server.MapPath("styleitalic.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String theText = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur." doc.Rect.Inset(20, 40) doc.TextStyle.Size = 96 doc.TextStyle.Italic = True doc.AddText(theText) doc.Save(Server.MapPath("styleitalic.pdf")) End Using ``` styleitalic.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>