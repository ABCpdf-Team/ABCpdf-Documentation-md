---
title: "02-textflow2"
css: "abcpdf-docs.css"
---

|  |  | Text Flow Round Image Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to flow text around an image. The techniques shown here may be used in conjunction with the Text Flow example which shows how to flow text between areas on the same or different pages. |  |  | 

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Setup</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| First we'll set up a convenient variable to contain the text we want to display. [C#] ```csharp // text truncated for clarity string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes..."; ``` [Visual Basic] ```vbnet ' text truncated for clarity Dim text As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes..." ``` |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Doc Obj</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Next we create an ABCpdf Doc object and give it our basic settings. We enlarge the line width, increase the font size, enable justification and inset the drawing rectangle from the edges of the document. [C#] ```csharp using var doc = new Doc(); doc.Width = 4; doc.FontSize = 32; doc.TextStyle.Justification = 1; doc.Rect.Inset(20, 20); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Width = 4 doc.FontSize = 32 doc.TextStyle.Justification = 1 doc.Rect.Inset(20, 20) ``` |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr>
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

      Image</td>
    <td>&nbsp;</td>
    <td valign="top">
| We save the rect since we're going to need it later. Then we add an image to the left hand side of the page. This is the image we are going to flow around. [C#] ```csharp string saveRect = doc.Rect.String; using var xi = XImage.FromFile(Server.MapPath("mypics/pic.jpg"), null); doc.Rect.Resize(xi.Width / 2, xi.Height / 2, XRect.Corner.TopLeft); doc.AddImage(xi); ``` [Visual Basic] ```vbnet Dim saveRect As String = doc.Rect.String Using xi As XImage = XImage.FromFile(Server.MapPath("mypics/pic.jpg"), Nothing) doc.Rect.Resize(xi.Width / 2, xi.Height / 2, XRect.Corner.TopLeft) doc.AddImage(xi) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  

    Text</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The crucial part occurs here which is where we set up the variable left margins to ensure that our text is shifted away from the image. If we had images on the right we would want to use variable right margins too. But here it is not necessary. [C#] ```csharp double padX = doc.FontSize; double padY = doc.FontSize / 3.0; string format = ""; string style = string.Format(format, doc.Rect.Height + padY, doc.Rect.Width + padX); ``` [Visual Basic] ```vbnet Dim padX As Double = doc.FontSize Dim padY As Double = doc.FontSize / 3.0 Dim format As String = "" Dim style As String = String.Format(format, doc.Rect.Height + padY, doc.Rect.Width + padX) ``` |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Save</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| After adding and framing our text we save the document to a specified location and clear our document. [C#] ```csharp doc.Rect.String = saveRect; doc.FrameRect(); int id = doc.AddTextStyled(style + text + ""); doc.Save(Server.MapPath("textflowroundimage.pdf")); ``` [Visual Basic] ```vbnet doc.Rect.String = saveRect doc.FrameRect() Dim id As Integer = doc.AddTextStyled(style + text + "") doc.Save(Server.MapPath("textflowroundimage.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| textflowroundimage.pdf |  |  | 
| --- | --- | --- |

    </td>
  </tr>
</table>