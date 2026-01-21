---
title: "addimagebitmap"
css: "abcpdf-docs.css"
---

|  |  | AddImageBitmap Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a System.Drawing.Bitmap to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddImageBitmap(System.Drawing.Bitmap bm, bool transparent) ``` [Visual Basic] ``` Function AddImageBitmap(bm As System.Drawing.Bitmap, transparent As Boolean) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| bm | A .NET Bitmap to be added to the page. | 
| transparent | Whether transparency information should be preserved. | 
| return | The ID of the newly added Image Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a System.Drawing.Bitmap to the current page. If the Transparent parameter is set to true then any transparency information will be preserved. This allows you to add formats such as transparent GIF and PNG with alpha channel. The image is scaled to fill the current Rect. It is transformed using the current Transform. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds a transparent PNG to a document. [C#] ```csharp using var doc = new Doc(); string path = Server.MapPath("../mypics/mypic.png"); using var bm = new Bitmap(path); doc.Rect.Inset(20, 20); doc.Color.String = "0 0 200"; doc.FillRect(); doc.AddImageBitmap(bm, true); bm.Dispose(); doc.Save(Server.MapPath("docaddimagebitmap.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim thePath As String = Server.MapPath("../mypics/mypic.png") Dim bm As New Bitmap(thePath) doc.Rect.Inset(20, 20) doc.Color.String = "0 0 200" doc.FillRect() doc.AddImageBitmap(bm, True) bm.Dispose() doc.Save(Server.MapPath("docaddimagebitmap.pdf")) End Using ``` docaddimagebitmap.pdf Also see example code in: XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering SaveAlpha Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>