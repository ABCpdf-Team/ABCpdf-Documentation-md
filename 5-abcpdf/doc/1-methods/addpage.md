---
title: "addpage"
css: "abcpdf-docs.css"
---

|  |  | AddPage Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a page to the current document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| [C#] ```csharp int AddPage(); int AddPage(int page); ``` [Visual Basic] ```vbnet Function AddPage() As Integer Function AddPage(page As Integer) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| page | The page insertion location. By default, pages are added at the end of the document. | 
| return | The Object ID of the newly added Page Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a page to the current document. The AddPage function returns the Object ID of the newly added Page Object. Typically, you will want to assign this return value to the document Page property using code of the form. [C#] ```csharp theDoc.Page = theDoc.AddPage(); ``` [Visual Basic] ```vbnet theDoc.Page = theDoc.AddPage() ``` Pages are added at the end of the document. However, you can use the page parameter to insert pages at other locations. The following code inserts a page at the start of a document. [C#] ```csharp theDoc.Page = theDoc.AddPage(1); ``` [Visual Basic] ```vbnet theDoc.Page = theDoc.AddPage(1) ``` Any existing page and all subsequent pages will be shifted towards the end of the document to make room for the insertion. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds three pages to a document. Each page is marked with the page number and page Object ID. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; // big text doc.TextStyle.HPos = 0.5; // centered doc.TextStyle.VPos = 0.5; // ... for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 ' big text doc.TextStyle.HPos = 0.5 ' centered doc.TextStyle.VPos = 0.5 ' ... Dim i As Integer = 1 While i docaddpage.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>