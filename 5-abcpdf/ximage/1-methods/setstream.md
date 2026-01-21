---
title: "setstream"
css: "abcpdf-docs.css"
---

|  |  | SetStream Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Load an image from stream. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetStream(Stream stream) ``` [Visual Basic] ``` Sub SetStream(stream As Stream) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| Stream | The stream containing the graphic. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Load an image from stream. The stream can contain any of the following types: JPEG, GIF, TIFF, BMP, PNG, PSD, PDB, EXIF, WMF, EMF, EPS, PS or SWF (Flash). Ultimately each import goes through a ReadModule so for details of additional formats supported and the way they are imported, see the ReadModule property. Different images within the file can be accessed using the Frame property. Different portions of the image can be selected using the Selection property. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we read a TIFF file and present the data to the XImage object. We then add the image to our document and then save the PDF. [C#] ```csharp using var img = new XImage(); string path = Server.MapPath("../mypics/mypic.jpg"); using var stream = File.OpenRead(path); img.SetStream(stream); using var doc = new Doc(); doc.Rect.Inset(20, 20); doc.AddImageObject(img, false); doc.Save(Server.MapPath("imagesetstream.pdf")); ``` [Visual Basic] ```vbnet Dim theImg As New XImage() Dim thePath As String thePath = Server.MapPath("../mypics/mypic.jpg") Dim theStream As Stream theStream = File.OpenRead(thePath) theImg.SetStream(theStream) theStream.Close() Dim doc As New Doc() doc.Rect.Inset(20, 20) doc.AddImageObject(theImg, False) theImg.Clear() doc.Save(Server.MapPath("imagesetstream.pdf")) doc.Clear() ``` imagesetstream.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>