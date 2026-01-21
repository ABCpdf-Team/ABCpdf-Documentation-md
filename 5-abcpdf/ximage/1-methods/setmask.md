---
title: "setmask"
css: "abcpdf-docs.css"
---

|  |  | SetMask Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Assign a soft mask to the image. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetMask(XImage mask, bool invert) ``` [Visual Basic] ``` Sub SetMask(mask As XImage, invert As Boolean) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| mask | The image containing the soft mask. | 
| invert | Whether to invert the mask. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Assign a soft mask or alpha channel. Soft masks are used to assign levels of transparency to an image. The mask provided will be converted to a grayscale intensity map and may be scaled to ensure that the dimensions of the mask match those of the image. The assigned mask applies to all frames of the current image. If the Invert parameter is set then the mask will be inverted - making transparent areas opaque and opaque areas transparent. Different images within the mask can be accessed using the Frame property. Different portions of the mask can be selected using the Selection property. Note that transparency is only applied to an Image if the Indirect property is true (which is generally the case). |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we read a TIFF file and present the data to the Image object. We then read a mask image and assign that to our Image. Finally we add the image to our document and then save the PDF. [C#] ```csharp using var doc = new Doc(); using var img = new XImage(); using var msk = new XImage(); img.SetFile(Server.MapPath("../mypics/mypic.jpg")); msk.SetFile(Server.MapPath("../mypics/mymask.jpg")); img.SetMask(msk, true); doc.Color.String = "0 0 0"; doc.FillRect(); doc.Rect.Inset(20, 20); doc.AddImageObject(img, true); doc.Save(Server.MapPath("imagesetmask.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim theImg As New XImage() Dim theMsk As New XImage() theImg.SetFile(Server.MapPath("../mypics/mypic.jpg")) theMsk.SetFile(Server.MapPath("../mypics/mymask.jpg")) theImg.SetMask(theMsk, True) theMsk.Clear() doc.Color.String = "0 0 0" doc.FillRect() doc.Rect.Inset(20, 20) doc.AddImageObject(theImg, True) theImg.Clear() doc.Save(Server.MapPath("imagesetmask.pdf")) End Using ``` Given the following input images. mypic.jpg | mymask.jpg | 
| --- | --- |

This is the kind of output you might expect.

![](../../../images/pdf/imagesetmask.pdf.png)imagesetmask.pdf

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>