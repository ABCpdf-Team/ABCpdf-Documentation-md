---
title: "addtext"
css: "abcpdf-docs.css"
---

|  |  | AddText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a block of single styled text to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddText(string text) ``` [Visual Basic] ``` Function AddText(text As String) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | The text to be added to the page. | 
| return | The Object ID of the newly added Text Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a block of single styled text to the current page. For adding multi-styled text or for chaining text from one page to another you should use the AddTextStyled method which is used for adding styled text. The text is in the current style, size and color and starts at the location specified in the current position. If the text is long it will will wrap and extend downwards until it fills the current rectangle. Text positioning in the rectangle is determined by the horizontal and vertical positioning. You can chain together multiple text blocks so that text flows from one to the next. To do this you need to first add a block of text using AddText. Then add multiple new text blocks using AddTextStyled each time passing in the ID obtained from the previous call after adjusting the target location (such as the rectangle or the page). The AddText function returns the Object ID of the newly added Text Object. If no text could be added then zero is returned. This will happen if a zero length string was supplied or if the rectangle was too small for even one character to be displayed. Typically you will get a return value of zero if your text was too large to fit in your Rect or if the Pos was at the end of the Rect. So if you are expecting text to be displayed and are seeing a return value of zero, check your text size, check your Rect is where you think it is by framing it using FrameRect and ensure your Pos is set at the top left of the Rect. Text is drawn word-wrapped within the current rectangle with the first character at the location specified by the Pos property. Normally the Pos property reflects the top left position of the current rectangle. However if you need to alter the position at which text drawing starts you can modify the Pos property after changing the Rect. When the text has been drawn the Pos will be updated to reflect the next text insertion point. Character positioning is specified from the top left of the character. Please see Pos for details on positioning when using vertical fonts. The FontSize determines the total line height and the character baseline is 80% of the way down from the top of the line. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds a number of chunks of text to a document. Each chunk is in a different style. This sample makes use of the fact that the Pos is updated to point to the next text insertion point after adding a piece of text. However note that when inserting muti-styled text it is generally more efficient to use the AddTextStyled method. [C#] ```csharp using var doc = new Doc(); doc.Page = doc.AddPage(); doc.FontSize = 48; int font1 = doc.AddFont("Times-Roman"); int font2 = doc.AddFont("Times-Bold"); doc.Font = font1; doc.AddText("Gallia est omnis "); doc.Font = font2; doc.AddText("tertiam Galli appellantur "); doc.Font = font1; doc.AddText("divisa in partes tres, "); doc.Font = font2; doc.AddText("quarum unam incolunt "); doc.Font = font1; doc.AddText("Belgae, aliam Aquitani. "); doc.Font = font2; doc.AddText("tertiam Galli appellantur"); doc.Save(Server.MapPath("docaddtext.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Page = doc.AddPage() doc.FontSize = 48 Dim theF1 As Integer = doc.AddFont("Times-Roman") Dim theF2 As Integer = doc.AddFont("Times-Bold") doc.Font = theF1 doc.AddText("Gallia est omnis ") doc.Font = theF2 doc.AddText("tertiam Galli appellantur ") doc.Font = theF1 doc.AddText("divisa in partes tres, ") doc.Font = theF2 doc.AddText("quarum unam incolunt ") doc.Font = theF1 doc.AddText("Belgae, aliam Aquitani. ") doc.Font = theF2 doc.AddText("tertiam Galli appellantur") doc.Save(Server.MapPath("docaddtext.pdf")) End Using ``` docaddtext.pdf Also see example code in: ABCpdf Deletion Example, ABCpdf Headers and Footers Example, ABCpdf Landscape Example, ABCpdf Unicode Example, ABCpdf eForm Placeholder Example, ABCpdf eForm FDF Example, ABCpdf Advanced Graphics Example, ABCpdf Fields, Markup and Movies Example, Doc AddBookmark Function, Doc AddColorSpaceFile Function, Doc AddColorSpaceSpot Function, Doc AddFont Function, Doc AddPage Function, Doc Append Function, Doc EmbedFont Function, Doc Read Function, Doc RemapPages Method, Doc Save Function, Doc Encryption Property, Doc Font Property, Doc FontSize Property, Doc Page Property, Doc Pos Property, Doc String Property, Doc TextStyle Property, Doc TopDown Property, Doc Transform Property, XColor Alpha Property, XEncryption SetCryptMethods Function, XHtmlOptions GetTagRects Function, XHtmlOptions HtmlCallback Property, XPoint Point Property, XRect Rectangle Property, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering IccCmyk Property, XRendering SaveAlpha Property, XTextStyle Bold Property, XTextStyle CharSpacing Property, XTextStyle HPos Property, XTextStyle Indent Property, XTextStyle Italic Property, XTextStyle Justification Property, XTextStyle LeftMargin Property, XTextStyle LineSpacing Property, XTextStyle Outline Property, XTextStyle ParaSpacing Property, XTextStyle Size Property, XTextStyle Strike Property, XTextStyle Strike2 Property, XTextStyle Underline Property, XTextStyle VPos Property, XTextStyle WordSpacing Property, XTransform Invert Function, XTransform Magnify Function, XTransform Reset Function, XTransform Rotate Function, XTransform AngleUnit Property, FileSpecification FileSpecification Function, FontObject Widths Property, Page VectorizeText Function, Signature Validate Function, ArrayAtom FromContentStream Function, XpsImportOperation Import Function, SwfImportOperation Import Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>