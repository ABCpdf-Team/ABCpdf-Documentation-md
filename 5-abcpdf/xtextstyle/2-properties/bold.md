---
title: "bold"
css: "abcpdf-docs.css"
---

|  |  | Bold Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to apply a synthetic bold effect. | 

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
      
| This property determines whether a synthetic bold effect is applied to text. It is generally better to specify a bold typeface rather than synthesize a bold effect using the current typeface. However under some circumstances this may not be possible and you may prefer to apply a synthetic bold effect. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we add some bold text to a document. [C#] ```csharp using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur."; doc.Rect.Inset(20, 40); doc.TextStyle.Size = 96; doc.TextStyle.Bold = true; doc.AddText(text); doc.Save(Server.MapPath("stylebold.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String theText = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur." doc.Rect.Inset(20, 40) doc.TextStyle.Size = 96 doc.TextStyle.Bold = True doc.AddText(theText) doc.Save(Server.MapPath("stylebold.pdf")) End Using ``` stylebold.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>