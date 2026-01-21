---
title: "font"
css: "abcpdf-docs.css"
---

|  |  | Font Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | No | The current Font ID. | 

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
      
| The font used for drawing text. This property holds the current Font ID and determines the style of text that is added to the document using methods like AddText. To get a Font ID you need to add your font to the current document using the AddFont method. The Font property is an accessor for the the XTextStyle.Font property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example adds two blocks of styled text to a document. The first block is in Helvetica and the second in Courier. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; // big text doc.Font = doc.AddFont("Helvetica"); doc.AddText("Helvetica Text."); doc.Font = doc.AddFont("Courier"); doc.AddText("Courier Text."); doc.Save(Server.MapPath("docfont.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 ' big text doc.Font = doc.AddFont("Helvetica") doc.AddText("Helvetica Text.") doc.Font = doc.AddFont("Courier") doc.AddText("Courier Text.") doc.Save(Server.MapPath("docfont.pdf")) End Using ``` docfont.pdf Also see example code in: ABCpdf Unicode Example, ABCpdf eForm Placeholder Example, ABCpdf eForm Stamp Example, ABCpdf eForm FDF Example, ABCpdf Fields, Markup and Movies Example, Doc AddFont Function, Doc AddText Function, Doc EmbedFont Function, Doc String Property, FontObject Widths Property, ArrayAtom FromContentStream Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>