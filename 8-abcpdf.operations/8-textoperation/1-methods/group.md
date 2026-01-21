---
title: "group"
css: "abcpdf-docs.css"
---

|  |  | Group Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Group a range of text fragments into a set of lines. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IListTextGroup> Group(ListTextFragment> fragments) ``` [Visual Basic] `Function Group(fragments As ListTextFragment>) As IListTextGroup>` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| fragments | The fragments to be grouped. | 
| Return | Returns a list of groups defining the words. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Group a range of text fragments into a set of lines. Calling Select will return a list of TextFragments corresponding to the section of text you are interested in. However each TextFragment may only make up a small portion of a word. Calling this function allows you to group connected fragments into continuous sections with a common rectangular area. Strictly speaking this grouping does not always correspond to lines. For example two fragments on the same line, separated by a large distance, will not be considered contiguous. However for most purposes the two broadly correspond. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we highlight a set of words in a source document by drawing a rectangle around each one. [C#] ```csharp string src = Server.MapPath("mypics/Acrobat.pdf"); string dst = Server.MapPath("HighlightedText.pdf"); string searchString = "Acrobat"; using var doc = new Doc(); doc.Read(src); TextOperation op = new TextOperation(doc); op.PageContents.AddPages(); string text = op.GetText(); int pos = 0; while (true) { pos = text.IndexOf(searchString, pos, StringComparison.CurrentCultureIgnoreCase); if (pos [Visual Basic] ```vbnet Dim theSrc As String = Server.MapPath("mypics/Acrobat.pdf") Dim theDst As String = Server.MapPath("HighlightedText.pdf") Dim searchString As String = "Acrobat" Using doc As New Doc() doc.Read(theSrc) Dim op As New TextOperation(doc) op.PageContents.AddPages() Dim text As String = op.GetText() Dim pos As Integer = 0 While True pos = text.IndexOf(searchString, pos, StringComparison.CurrentCultureIgnoreCase) If pos |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>