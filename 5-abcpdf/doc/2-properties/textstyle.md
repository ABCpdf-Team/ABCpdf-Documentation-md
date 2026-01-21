---
title: "textstyle"
css: "abcpdf-docs.css"
---

|  |  | TextStyle Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp XTextStyle ``` [Visual Basic] `XTextStyle` | Ten point text. | No | The current style for drawing text. | 

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
      
| This property determines the current style settings used for adding text. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code creates a PDF document and adds some text using a number of the text style properties to control formatting. [C#] ```csharp using var doc = new Doc(); string text = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes lingua, institutis, legibus inter se differunt. Gallos ab Aquitanis Garumna flumen, a Belgis Matrona et Sequana dividit."; text = text + "\r\n" + text + "\r\n" + text + "\r\n"; doc.Rect.Inset(20, 20); doc.TextStyle.Size = 32; doc.TextStyle.Justification = 1; doc.TextStyle.Indent = 64; doc.TextStyle.ParaSpacing = 32; doc.AddText(text); doc.Save(Server.MapPath("doctextstyle.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theText As String = "Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur. Hi omnes lingua, institutis, legibus inter se differunt. Gallos ab Aquitanis Garumna flumen, a Belgis Matrona et Sequana dividit." theText = theText + vbCr & vbLf + theText + vbCr & vbLf + theText + vbCr & vbLf doc.Rect.Inset(20, 20) doc.TextStyle.Size = 32 doc.TextStyle.Justification = 1 doc.TextStyle.Indent = 64 doc.TextStyle.ParaSpacing = 32 doc.AddText(theText) doc.Save(Server.MapPath("doctextstyle.pdf")) End Using ``` doctextstyle.pdfAlso see example code in: ABCpdf Text Flow Example, ABCpdf Text Flow Round Image Example, ABCpdf Deletion Example, ABCpdf Headers and Footers Example, Doc AddPage Function, Doc Append Function, Doc Read Function, Doc RemapPages Method, XRendering SaveAlpha Property, XTextStyle Bold Property, XTextStyle CharSpacing Property, XTextStyle HPos Property, XTextStyle Indent Property, XTextStyle Italic Property, XTextStyle Justification Property, XTextStyle Kerning Property, XTextStyle LeftMargin Property, XTextStyle LineSpacing Property, XTextStyle Outline Property, XTextStyle ParaSpacing Property, XTextStyle Size Property, XTextStyle Strike Property, XTextStyle Strike2 Property, XTextStyle Underline Property, XTextStyle VPos Property, XTextStyle WordSpacing Property, XTransform Rotate Function, XTransform AngleUnit�Property, FontObject Widths Property, Page GetBitmap Function, XpsImportOperation Import Function, SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>