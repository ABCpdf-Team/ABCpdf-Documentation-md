---
title: "gettagrects"
css: "abcpdf-docs.css"
---

|  |  | GetTagRects Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets an array of the locations of tagged visible items. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp XRect[] GetTagRects(int id) ``` [Visual Basic]`Function GetTagRects(id As Integer) As XRect()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the object. | 
| return | The location of tagged visible HTML objects. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to retrieve the locations of tagged visible items. The locations are to be used with Doc.Transform being identity. To use this method you need to enable the tagging functionality. See the AddTags property for details. This function takes an ID obtained from a call to Doc.AddImageUrl, Doc.AddImageHtml or Doc.AddImageToChain and returns the locations of any items which are visible on the PDF page as a result of that call. The locations match up directly on a one-to-one basis with the IDs returned by the GetTagIDs function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following example shows the effect that this parameter has on HTML rendering. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(100, 100); doc.Rect.Top = 700; doc.HtmlOptions.Engine = EngineType.Chrome123; doc.HtmlOptions.AddTags = true; // The ABCGecko and MSHTML tagging format uses styles. string html1 = "" + "" + ".tag-visible { abcpdf-tag-visible:true; outline: 1px solid transparent; font-size: 72pt; }" + "" + "" + "Gallia est omnis divisa in partes tres." + ""; // The ABCChrome tagging format uses attributes. string html2 = "" + "" + "p { font-size: 72pt; }" + "" + "" + "Gallia est omnis divisa in partes tres." + ""; string html = doc.HtmlOptions.Engine != EngineType.Chrome123 ? html1 : html2; int id = doc.AddImageHtml(html); // Frame location of the tagged element var tagRects = doc.HtmlOptions.GetTagRects(id); foreach (var rect in tagRects) { doc.Rect.String = rect.ToString(); doc.FrameRect(); } // Output tag ID var tagIds = doc.HtmlOptions.GetTagIDs(id); doc.Rect.String = doc.MediaBox.String; doc.Rect.Inset(20, 20); doc.FontSize = 64; doc.Color.String = "255 0 0"; doc.AddText($"Tag ID \"{tagIds[0]}\":"); // Save the document doc.Save(Server.MapPath("HtmlOptionsGetTagRects.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(100, 100) doc.Rect.Top = 700 doc.HtmlOptions.Engine = EngineType.Chrome123 doc.HtmlOptions.AddTags = True ' The ABCGecko and MSHTML tagging format uses styles. Dim html1 As String = "" + "" + ".tag-visible { abcpdf-tag-visible:true; outline: 1px solid transparent; font-size: 72pt; }" + "" + "" + "Gallia est omnis divisa in partes tres." + "" ' The ABCChrome tagging format uses attributes. Dim html2 As String = "" + "" + "p { font-size: 72pt; }" + "" + "" + "Gallia est omnis divisa in partes tres." + "" Dim html As String = If(doc.HtmlOptions.Engine <> EngineType.Chrome123, html1, html2) Dim id As Integer = doc.AddImageHtml(html) ' Frame location of the tagged element Dim tagRects As XRect() = doc.HtmlOptions.GetTagRects(id) For Each theRect As XRect In tagRects doc.Rect.String = theRect.ToString() doc.FrameRect() Next ' Output tag ID Dim tagIds As String() = doc.HtmlOptions.GetTagIDs(id) doc.Rect.String = doc.MediaBox.[String] doc.Rect.Inset(20, 20) doc.FontSize = 64 doc.Color.String = "255 0 0" doc.AddText($"Tag ID ""{tagIds[0]}"":") ' Save the document doc.Save(Server.MapPath("HtmlOptionsGetTagRects.pdf")) End Using ``` HtmlOptionsGetTagRects.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>