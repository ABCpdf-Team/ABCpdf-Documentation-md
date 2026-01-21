---
title: "addbookmark"
css: "abcpdf-docs.css"
---

|  |  | AddBookmark Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a bookmark pointing to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| [C#] ```csharp int AddBookmark(string path, bool open); ``` [Visual Basic] ```vbnet Function AddBookmark(path As String, open As Boolean) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The path to the bookmark. | 
| open | Whether the bookmark should be displayed open (expanded) or closed (collapsed). | 
| return | The Object ID of the newly added Bookmark Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a bookmark which points to the current page. Bookmarks are specified as paths in much the same way as file paths. Headings and subheadings are separated by a backslash character. For example: "1. Introduction\1.1 Aim and Methods\1.1.3 Diagrams" When a bookmark is added, intermediate headings and subheadings will be created if they do not already exist. To add multiple bookmarks all referring to the same page simply call the AddBookmark function multiple times. This function returns the Object ID of the newly added Bookmark Object. Hyperlinks. Sometimes you may wish to insert bookmarks which link to an external web page specified using a URI or URL. You can do this using hyperlink code of the following form. Please do ensure that your URLs come from trusted sources only. You do not want to be in a situation in which people can add links to malware or other dubious locations. [C#] ```csharp static int AddBookmarkToUri(Doc doc, string bookmark, string uri) { int id = doc.AddBookmark(bookmark, true); doc.SetInfo(id, "/Dest:Del", ""); // remove link to page and add link to url doc.SetInfo(id, "/A", ">"); doc.SetInfo(id, "/A/URI:Text", uri); return id; } ``` [Visual Basic] ```vbnet Private Shared Function AddBookmarkToUri(ByVal doc As Doc, ByVal bookmark As String, ByVal uri As String) As Integer Dim id As Integer = doc.AddBookmark(bookmark, True) doc.SetInfo(id, "/Dest:Del", "", "") ' remove link to page and add link to url doc.SetInfo(id, "/A", ">") doc.SetInfo(id, "/A/URI:Text", uri) Return id End Function ``` | 
| --- |

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds a sequence of pages with a nested sequence of bookmarks. The image shows the appearance of the document outline. Note that none of the subject pages are visible because the chapter pages were added in a collapsed state. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 64; for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 64 Dim i As Integer = 1 While i docaddbookmark.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>