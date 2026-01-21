---
title: "underline"
css: "abcpdf-docs.css"
---

|  |  | Underline Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to underline text. | 

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
      
| This property determines whether underlining is applied to text. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| In this example we add some underlined text to a document. [C#] ```csharp using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur."; doc.Rect.Inset(20, 40); doc.TextStyle.Size = 96; doc.TextStyle.Underline = true; doc.AddText(text); doc.Save(Server.MapPath("styleunderline.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur." doc.Rect.Inset(20, 40) doc.TextStyle.Size = 96 doc.TextStyle.Underline = True doc.AddText(theText) doc.Save(Server.MapPath("styleunderline.pdf")) End Using ``` styleunderline.pdf Also see example code in: XTransform AngleUnit�Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>