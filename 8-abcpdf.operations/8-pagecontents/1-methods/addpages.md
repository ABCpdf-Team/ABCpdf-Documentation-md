---
title: "addpages"
css: "abcpdf-docs.css"
---

|  |  | AddPages Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add pages to be processed. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void AddPages() void AddPages(int pageNumber) void AddPages(int startPageNumber, int endPageNumber) ``` [Visual Basic] ``` Sub AddPages() Sub AddPages(pageNumber As Integer) Sub AddPages(startPageNumber As Integer, endPageNumber As Integer) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| pageNumber | The number of the page to be processed. This is a one based index. | 
| startPageNumber | The number of the first page to be processed. This is a one based index. | 
| endPageNumber | The number of the last page to be processed. This is a one based index. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method adds pages that need to be processed. If the provided page numbers are incorrect then an exception will be raised. The parameterless version of this function adds all the pages in the document. If you are only interested in a subsection of the document you can specify individual pages or a range of pages using the overloads. You can call this function multiple times with multiple sets of pages to get the precise selection that you require. Adding pages is a fairly expensive operation. For this reason if you are performing multiple types of analysis on the same set of pages then you will probably want to share one PageContents object between them. Note that the PageContents object is a cache of the current document content. Thus it may be invalidated by a call that remaps or replaces existing content in the document. For this reason you should not call Doc.Save, Doc.GetData or Doc.Flatten while using an operation that contains a PageContents object. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See TextOperation.Group. Also see example code in: TextOperation Group Function, ImageOperation GetImageProperties Function, AccessibilityOperation AccessibilityOperation Constructor. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>