---
title: "addimagetochain"
css: "abcpdf-docs.css"
---

|  |  | AddImageToChain Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a new page from a paged HTML or PostScript render. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddImageToChain(int id) ``` [Visual Basic] ``` Function AddImageToChain(id As Integer) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The ID of the previous object in the chain. | 
| return | The ID of the newly added object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Some web pages are too large to fit on one PDF page. To split a web page across multiple PDF pages you need to call AddImageUrl or AddImageHtml to render the first page. The ID returned from these calls represents the head of the chain. To add subsequent pages to the chain you need to make calls to AddImageToChain passing in the previous image from the chain each time. As well as using chaining to split web pages across multiple PDF pages you can also use it to split your web pages across multiple columns within a page. You can even split your chain to generate multiple copies of the same page. More information can be found in the HTML / CSS Rendering section of the documentation. Similarly some PostScript (PS) files contain more than one page of content. To split a PS file across multiple PDF pages you need to call AddImageFile or AddImageData to render the first page. The ID returned from these calls represents the head of the chain. To add subsequent pages to the chain you need to make calls to AddImageToChain passing in the previous image from the chain each time. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This example shows how to import an HTML page into a multi-page PDF document. We first create a Doc object and inset the edges a little so that the HTML will appear in the middle of the page. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(72, 144); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(72, 144) ``` We add the first page of HTML. We save the returned ID as this will be used to add subsequent pages. [C#] ```csharp int id = doc.AddImageUrl("http://www.yahoo.com/"); ``` [Visual Basic] ```vbnet Dim theID As Integer theID = doc.AddImageUrl("http://www.yahoo.com/") ``` We now chain subsequent pages together. We stop when we reach a page which wasn't truncated. [C#] ```csharp while (true) { doc.FrameRect(); if (!doc.Chainable(id)) break; doc.Page = doc.AddPage(); id = doc.AddImageToChain(id); } ``` [Visual Basic] ```vbnet While True doc.FrameRect() If Not doc.Chainable(theID) Then Exit While End If doc.Page = doc.AddPage() theID = doc.AddImageToChain(theID) End While ``` After adding the pages we can flatten them. We can't do this until after the pages have been added because flattening will invalidate our previous ID and break the chain. [C#] ```csharp for (int i = 1; i [Visual Basic] ```vbnet Dim i As Integer = 1 While i Finally we save. [C#] ```csharp doc.Save(Server.MapPath("paged_html.pdf")); ``` [Visual Basic] ```vbnet doc.Save(Server.MapPath("paged_html.pdf")) End Using ``` We get the following output. paged_html.pdf [Page 1] | paged_html.pdf [Page 2] | 
| --- | --- |

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>