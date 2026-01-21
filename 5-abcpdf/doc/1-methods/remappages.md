---
title: "remappages"
css: "abcpdf-docs.css"
---

|  |  | RemapPages Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Remaps pages for reordering, copying and deletion. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void RemapPages(string pages) void RemapPages(int[] pages) void RemapPages(int[] pages, int index, int count) ``` [Visual Basic] ``` Sub RemapPages(pages As String) Sub RemapPages(pages() As Integer) Sub RemapPages(pages() As Integer, index As Integer, count As Integer) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| pages | The list of page numbers. | 
| index | The index of the first page number into the array pages. | 
| count | The number of page numbers in the array pages to use. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method provides a simple method for remapping the pages in a document. It can be used for reordering, copying or deleting pages. It accepts a list of page numbers and reorders the pages in the document so that they match these page numbers. If a number is repeated more than once, the page is duplicated. If a number is omitted, the page is deleted. Page numbers can be delimited using spaces, commas or semicolons. The first page in a document is page one. So to reverse a four page document, you might use "4 3 2 1". If a page is duplicated and it contains Form fields, you may want to call MakeFieldsUnique to avoid sharing fields across pages. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code snippet illustrates how one might reverse all the pages in a document. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); doc.FontSize = 500; doc.Color.String = "255 0 0"; doc.TextStyle.HPos = 0.5; doc.TextStyle.VPos = 0.3; int count = doc.PageCount; var pages = new List(); for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) doc.FontSize = 500 doc.Color.String = "255 0 0" doc.TextStyle.HPos = 0.5 doc.TextStyle.VPos = 0.3 Dim theCount As Integer = doc.PageCount Dim pages As New List(Of Integer)() Dim i As Integer = 1 While i docremappages.pdf [Page 1] | docremappages.pdf [Page 2] | 
| --- | --- |
| docremappages.pdf [Page 3] | docremappages.pdf [Page 4] | 

Also see example code in: [OpAtom Find Function](../../../7-abcpdf.atoms/opatom/1-methods/find.md).

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>