---
title: "recolor"
css: "abcpdf-docs.css"
---

|  |  | Recolor Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Converts the image from one color space to another. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Recolor(ColorSpace space) void Recolor(ColorSpace space, RenderingIntent intent) ``` [Visual Basic] ``` Sub Recolor(space As ColorSpace) Sub Recolor(space As ColorSpace, intent As RenderingIntent) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| space | The destination color space. | 
| intent | The rendering intent enumeration. If no intent is provided the default for the image (typically RelativeColorimetric) is used. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Converts the image from one color space to another. Calling this method results in the pixels within the PixMap image being mapped from the current color space to the new color space. The new ColorSpace is then assigned to the PixMap and (if it is not already there) added to the PixMap ObjectSoup. Colors can only be sensibly mapped from one color space to another if we know something about the characteristics of the color space. If your color spaces do not contain this information (e.g. if they are device color spaces) then ABCpdf will use a default color profile. An exception will be thrown if the operation is not possible. This may happen if the PixMap is not in an ObjectSoup or if the ColorSpace object is in some way invalid. If the ImageMask property is true the image has no color space and is implicitly black and white. Image masks cannot be anything other than black and white so trying to convert an image mask to another color space will result in an exception being raised. The rendering intent determines how out of gamut colors are handled. For full details see the RecolorOperation.RenderingIntent property. After the PixMap has been Recolored it is no longer compressed and will have a BitsPerComponent of eight or sixteen. You may wish to compress it using the StreamObject.Compress method. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we change all the images in a document to CMYK. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../Rez/spaceshuttle.pdf")); List theList = new List(); // find all the PixMap objects in the soup foreach (IndirectObject obj in doc.ObjectSoup) { var p = obj as PixMap; if (p != null) theList.Add(p); } // add our destination color space var cs = new ColorSpace(doc.ObjectSoup); cs.IccProfile = new IccProfile(doc.ObjectSoup, Server.MapPath("../Rez/abccmyk.icc")); // convert images to our color space for (int i = 0; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../Rez/spaceshuttle.pdf")) Dim theList As New List(Of PixMap)() ' find all the PixMap objects in the soup For Each obj As IndirectObject In doc.ObjectSoup Dim p As PixMap = TryCast(obj, PixMap) If p <> Nothing Then theList.Add(p) End If Next ' add our destination color space Dim cs As New ColorSpace(doc.ObjectSoup) cs.IccProfile = New IccProfile(doc.ObjectSoup, Server.MapPath("../Rez/abccmyk.icc")) ' convert images to our color space Dim i As Integer = 0 While i spaceshuttle.pdf [page 1] pixmaprecolor.pdf [page 1] |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>