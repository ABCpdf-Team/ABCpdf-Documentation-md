---
title: "getimageproperties"
css: "abcpdf-docs.css"
---

|  |  | GetImageProperties Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the image information for all the raster images. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IListImageProperties> GetImageProperties() ``` [Visual Basic] `Function GetImageProperties() As IListImageProperties>` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| Return | A collection of all the image properties.. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Get the image information for all the raster images. If the PageContents is null then an exception will be raised. After retrieving image properties you can iterate through them to find out information about what images there are and how they are placed in the document. Much like HTML, PDF allows a divorce between the image and the placement of that image. So you may have one PixMap which is drawn multiple times at multiple sizes in different locations within the document. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we highlight a set of images in a source document by drawing a red rectangle around each one. [C#] ```csharp string src = Server.MapPath("mypics/Acrobat.pdf"); string dst = Server.MapPath("HighlightedImages.pdf"); using var doc = new Doc(); doc.Read(src); doc.Color.SetRgb(255, 0, 0); doc.Width = 0.1; var op = new ImageOperation(doc); op.PageContents.AddPages(); var images = op.GetImageProperties(); foreach (var img in images) { foreach (var rend in img.Renditions) { rend.Focus(); doc.FrameRect(); } } doc.Save(dst); ``` [Visual Basic] ```vbnet Dim theSrc As String = Server.MapPath("mypics/Acrobat.pdf") Dim theDst As String = Server.MapPath("HighlightedImages.pdf") Using doc As New Doc() doc.Read(theSrc) doc.Color.SetRgb(255, 0, 0) doc.Width = 0.1 Dim op As New ImageOperation(doc) op.PageContents.AddPages() Dim images As IList(Of ImageProperties) = op.GetImageProperties() For Each pl As ImageProperties In images For Each plc As ImageRendition In pl.Renditions plc.Focus() doc.FrameRect() Next Next doc.Save(theDst) End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>