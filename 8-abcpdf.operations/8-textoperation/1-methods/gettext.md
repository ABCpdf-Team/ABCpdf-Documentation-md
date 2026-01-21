---
title: "gettext"
css: "abcpdf-docs.css"
---

|  |  | GetText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get all the text in the page contents. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string GetText() string GetText(XRect rect, int pageNumber) string GetText(XRect[] rects, int[] pageNumbers) ``` [Visual Basic] ``` Function GetText() As String Function GetText(rect As XRect, pageNumber As Integer) As String Function GetText(rects As XRect(), pageNumbers As Integer()) As String ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| rect | The rectangle from which to return text. | 
| rects | A set of rectangles forming a union from which to return text. | 
| pageNumber | The page number - a one based index. | 
| Return | The text. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method returns the text of the content that has been assigned via the PageContents. If the PageContents is null then an exception will be raised. The overloads of this function allow you to select an area of interest in terms of an area defined by single rectangle or by a union of multiple rectangles. They also allow you to select a subset of pages from which text should be returned. This page array is a set of page numbers - one based indexes - for which order is not important. Passing null for these parameters defaults to the entire page and the entire set of available pages respectively. The process of getting the text involves scanning through the text fragments in the document and joining them up dependent on their positions and sizes. The result is a standard string with line ends where the line ends in the document have been found. If there are parts of this string that you are interested in you can use the offset and length of the selections in conjunction with the Select method to identify those portions within the document. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Group function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>