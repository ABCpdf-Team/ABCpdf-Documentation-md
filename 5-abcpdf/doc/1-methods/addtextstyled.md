---
title: "addtextstyled"
css: "abcpdf-docs.css"
---

|  |  | AddTextStyled Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a block of multi-styled text to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddTextStyled(string text) int AddTextStyled(string dummy, int chainid) ``` [Visual Basic] ``` Function AddTextStyled(text As String) As Integer Function AddTextStyled(dummy As String, chainid As Integer) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | The HTML to be added to the page. | 
| dummy | A dummy parameter. The contents are not used. | 
| chainid | The Object ID of a previously added text block. | 
| return | The Object ID of the newly added Text Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a block of multi-styled text to the current page. This function works in a similar manner to the AddText function but it allows you to add multi-styled text by inserting simple HTML tags. A listing of supported tags is given in the Styled Text section of the documentation. Please see Pos for details on positioning when using vertical fonts. You can chain together multiple text/HTML blocks so that text flows from one to the next. To do this you need to first add a block of text/HTML using AddText or AddTextStyled. Then add multiple new text/HTML blocks using Doc.AddTextStyled each time passing in the ID obtained from the previous call after adjusting the target location (such as the rectangle or the page). When no more text is available the AddTextStyled function will return zero. Alternatively you can query the TextLayer.Truncated property of the returned object before adding a new item to the chain. This function returns the Object ID of the newly added Text Object. If no text could be added then zero is returned. This will happen if a zero length string was supplied or if the rectangle was too small for even one character to be displayed. Typically you will get a return value of zero if your text was too large to fit in your Rect or if the Pos was at the end of the Rect. Text styles for the entire HTML content are determined at the point at which the first item in a text chain is created. This means that varying document styles will not affect the way in which subsequent items in the chain are displayed. For an example of chaining see the Text Flow Example. Note that there is no requirement that blocks be organized in a linear chain. If you wish you can create trees of HTML blocks, flowing text from a chain head through multiple display areas on your document. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds some styled text to a document. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 72; doc.AddTextStyled("Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur."); doc.Save(Server.MapPath("docaddhtml.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 72 doc.AddTextStyled("Gallia est omnis divisa in partes tres, quarum unam incolunt Belgae, aliam Aquitani, tertiam qui ipsorum lingua Celtae, nostra Galli appellantur.") doc.Save(Server.MapPath("docaddhtml.pdf")) End Using ``` docaddhtml.pdf Also see example code in: ABCpdf Multistyle Example, XTextStyle Kerning Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>