---
title: "recolor"
css: "abcpdf-docs.css"
---

|  |  | Recolor Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Recolor pages in a document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Recolor(Doc doc) void Recolor(Pages pages) void Recolor(Page page) ``` [Visual Basic] ``` Sub Recolor(doc As Doc) Sub Recolor(pages As Pages) Sub Recolor(page As Page) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | The document to be recolored. | 
| pages | The pages to be recolored as referenced by a Pages IndirectObject. | 
| page | The page to be recolored as referenced by a Page IndirectObject. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Converts the specified pages from one color space to another. The destination color space is specified by assigning a value to the DestinationColorSpace property. All images used on the page are converted to the new color space. All color operators used in the page content stream are converted to the new color space. Annotations and fields are not part of the page but instead float over the page. You can choose whether to convert the appearance stream of any annotations or leave them in their native color space. This is controlled using the ConvertAnnotations property. Colors can only be sensibly mapped from one color space to another if we know something about the characteristics of the color space. If your color spaces do not contain this information (e.g. if they are device color spaces) then ABCpdf will use a default color profile. An exception will be thrown if the operation is not possible. This may happen if the IndirectObjects provided are not in an ObjectSoup or if the destination ColorSpace is in some way invalid. As part of the Recolor process, all images used on the page(s) are also recolored. (See also PixMap.Recolor.) After the recolor process has been completed these PixMap objects will no longer be compressed. You may wish to analyse and recompress these images by pre and post processing them during the ProcessingObject and ProcessedObject events. Although the Recolor operation is designed to convert a document to a single color space, such as CMYK, with actual colors unchanged, it can also be used to convert a document to a single, different, color. When you add a spot color (please see AddColorSpaceSpot) and make it the destination color space, the conversion will be to shades of the spot color specified. | 
| --- |

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we recolor one page out of a document. We pick up the ProcessingObject events so that we can store the source color space for all the PixMap objects which are processed. We do not want to convert CMYK pixmaps so we set the Cancel property to true if we find these. We then pick up the ProcessedObject events so that we can recompress the PixMap objects after they have been recolored. We vary the recompression method used dependent on the source color space and the size of the image. Here we use standard delegates for backwards compatibility with older code. However anonymous delegates will provide a more compact solution. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); MyOp.Recolor(doc, (Page)doc.ObjectSoup[doc.Page]); doc.Save(Server.MapPath("RecolorOperation.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) MyOp.Recolor(doc, DirectCast(doc.ObjectSoup(doc.Page), Page)) doc.Save(Server.MapPath("RecolorOperation.pdf")) End Using ``` [C#] ```csharp class MyOp { public static void Recolor(Doc doc, Page page) { var op = new RecolorOperation(); op.DestinationColorSpace = new ColorSpace(doc.ObjectSoup, ColorSpaceType.DeviceGray); op.ConvertAnnotations = false; op.ProcessingObject += Recoloring; op.ProcessedObject += Recolored; op.Recolor(page); } public static void Recoloring(object sender, ProcessingObjectEventArgs e) { var pm = e.Object as PixMap; if (pm != null) { ColorSpaceType cs = pm.ColorSpaceType; if (cs == ColorSpaceType.DeviceCMYK) e.Cancel = true; e.Tag = cs; } } public static void Recolored(object sender, ProcessedObjectEventArgs e) { if (e.Successful) { var pm = e.Object as PixMap; if (pm != null) { ColorSpaceType cs = (ColorSpaceType)e.Tag; if (pm.Width > 1000) pm.CompressJpx(30); else if (cs == ColorSpaceType.DeviceRGB) pm.CompressJpeg(30); else pm.Compress(); // Flate } } } } ``` [Visual Basic] ```vbnet Private Class MyOp Public Shared Sub Recolor(doc As Doc, page As Page) Dim op As New RecolorOperation() op.DestinationColorSpace = New ColorSpace(doc.ObjectSoup, ColorSpaceType.DeviceGray) op.ConvertAnnotations = False op.ProcessingObject += Recoloring op.ProcessedObject += Recolored op.Recolor(page) End Sub Public Shared Sub Recoloring(sender As Object, e As ProcessingObjectEventArgs) Dim pm As PixMap = TryCast(e.[Object], PixMap) If pm <> Nothing Then Dim cs As ColorSpaceType = pm.ColorSpaceType If cs = ColorSpaceType.DeviceCMYK Then e.Cancel = True End If e.Tag = cs End If End Sub Public Shared Sub Recolored(sender As Object, e As ProcessedObjectEventArgs) If e.Successful Then Dim pm As PixMap = TryCast(e.[Object], PixMap) If pm <> Nothing Then Dim cs As ColorSpaceType = DirectCast(e.Tag, ColorSpaceType) If pm.Width > 1000 Then pm.CompressJpx(30) ElseIf cs = ColorSpaceType.DeviceRGB Then pm.CompressJpeg(30) Else pm.Compress() ' Flate End If End If End If End Sub End Class ``` Also see example code in: RecolorOperation IccCmyk Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>