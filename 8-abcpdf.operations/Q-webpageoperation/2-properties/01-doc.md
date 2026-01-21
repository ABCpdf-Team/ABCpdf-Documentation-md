---
title: "01-doc"
css: "abcpdf-docs.css"
---

|  |  | Doc Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Doc ``` [Visual Basic] `Doc` | n/a | No | The Doc object on which to operate. | 

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
      
| The Doc object on which to operate. On creation of the WebPageOperation this property will be populated with a new Doc object. Set the Doc.MediaBox to select a page size. Select a Doc.Rect to set the content area. Items outside the Doc.Rect become margins and can be used for headers and footers. You can set Doc.HtmlOptions properties to specify features you wish to use. For calls like GetTagIDs or GetTagRects you can pass the relevant Doc.Page to select the specific page you require. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code creates a PDF document from HTML and outlines any tagged areas. [C#] ```csharp var op = new WebPageOperation(); using (op.Doc) { op.Doc.Rect.Inset(72, 72); op.Doc.HtmlOptions.AddTags = true; op.Doc.HtmlOptions.RetryCount = 0; op.Tagged = true; op.Outline = true; string template = "*"; op.HeaderHtml = template.Replace("*", "Commentarii de Bello Gallico"); op.FooterHtml = template.Replace("*", " of "); op.ReadUrl(GetUrl("commentarii.htm")); var tagIDs = op.Doc.HtmlOptions.GetTagIDs(op.Doc.Page); var tagRects = op.Doc.HtmlOptions.GetTagRects(op.Doc.Page); for (int i = 0; i [Visual Basic] ```vbnet Dim op = New WebPageOperation() Using op.Doc op.Doc.Rect.Inset(72, 72) op.Doc.HtmlOptions.AddTags = True op.Doc.HtmlOptions.RetryCount = 0 op.Tagged = True op.Outline = True Dim template As String = "*" op.HeaderHtml = template.Replace("*", "Commentarii de Bello Gallico") op.FooterHtml = template.Replace("*", " of ") op.ReadUrl(GetUrl("commentarii.htm")) Dim tagIDs = op.Doc.HtmlOptions.GetTagIDs(op.Doc.Page) Dim tagRects = op.Doc.HtmlOptions.GetTagRects(op.Doc.Page) Dim i As Integer = 0 While i |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>