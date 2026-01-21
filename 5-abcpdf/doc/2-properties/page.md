---
title: "page"
css: "abcpdf-docs.css"
---

|  |  | Page Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | No | The current Page ID. | 

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
      
| This property holds the current Page Object ID. It is important to note that the Page property is different to the PageNumber property. Either the Page or the PageNumber property can be used to set the current page. The Page holds an Object ID typically returned from a call to AddPage. The PageNumber indicates the page using an index ranging between one and the PageCount. Do not set the Page property to a page number. If you have a page number you want to be using the PageNumber property. The current page is the one that receives new objects as they are added to the document. For example the methods AddText, AddLine, AddImage, FrameRect and FillRect all operate on the current page. When you change the Page property the Pos property is reset to the top left of the current Rect. If no page is specified the current page is taken to be the first page in the document. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example creates a document with two pages and adds text to each of the pages in turn. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; // big text doc.Page = doc.AddPage(); doc.AddText("Page One"); doc.Page = doc.AddPage(); doc.AddText("Page Two"); doc.Save(Server.MapPath("docpage.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 ' big text doc.Page = doc.AddPage() doc.AddText("Page One") doc.Page = doc.AddPage() doc.AddText("Page Two") doc.Save(Server.MapPath("docpage.pdf")) End Using ``` docpage.pdf Also see example code in: ABCpdf Text Flow Example, ABCpdf Headers and Footers Example, ABCpdf Unicode Example, ABCpdf Paged HTML Example, ABCpdf Fields, Markup and Movies Example, Doc AddBookmark Function, Doc AddGrid Function, Doc AddImageDoc Function, Doc AddImageToChain Function, Doc AddPage Function, Doc AddText Function, Doc MediaBox Property, XForm AddDocTimestamp Function, XHtmlOptions LinkDestinations Method, XHtmlOptions LinkPages Method, XHtmlOptions UseScript Property, XImage Frame Property, XTextStyle Kerning Property, XTransform AngleUnit Property, Page MakeFormXObject Function, Page Rotation Property, Page Thumbnail Property, Signature AddLTV Function, XpsImportOperation Import Function, SwfImportOperation Import Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>