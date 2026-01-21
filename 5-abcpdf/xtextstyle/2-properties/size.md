---
title: "size"
css: "abcpdf-docs.css"
---

|  |  | Size Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic] `Double` | 10.0 | No | The current text size. | 

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
      
| This property determines the size of text that is added to the document using the AddText and AddTextStyled methods. The Size property is equivalent to the the Doc.FontSize property but unlike the FontSize property it allows fractional point sizes to be specified. The font size is measured in units. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example adds two blocks of styled text to a document. The first block is in 96.5 point type and the second is in 192.5 point type. [C#] ```csharp using var doc = new Doc(); doc.TextStyle.Size = 96.5; doc.AddText("Small "); doc.TextStyle.Size = 192.5; doc.AddText("Big"); doc.Save(Server.MapPath("stylesize.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.TextStyle.Size = 96.5 doc.AddText("Small ") doc.TextStyle.Size = 192.5 doc.AddText("Big") doc.Save(Server.MapPath("stylesize.pdf")) End Using ``` stylesize.pdf Also see example code in: Doc TextStyle Property, XTextStyle Bold Property, XTextStyle CharSpacing Property, XTextStyle Indent Property, XTextStyle Italic Property, XTextStyle Justification Property, XTextStyle Kerning Property, XTextStyle LeftMargin Property, XTextStyle LineSpacing Property, XTextStyle Outline Property, XTextStyle ParaSpacing Property, XTextStyle Strike Property, XTextStyle Strike2 Property, XTextStyle Underline Property, XTextStyle WordSpacing Property, Page GetBitmap Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>