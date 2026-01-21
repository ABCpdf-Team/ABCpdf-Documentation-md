---
title: "setfile"
css: "abcpdf-docs.css"
---

|  |  | SetFile Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Load an image from a file. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetFile(string path) ``` [Visual Basic] ``` Sub SetFile(path As String) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The path to the graphic file. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Load an image from file. The file can be any of the following types: JPEG, GIF, TIFF, BMP, PNG, PSD, PDB, EXIF, WMF, EMF, EPS, PS or SWF (Flash). Ultimately each import goes through a ReadModule so for details of additional formats supported and the way they are imported, see the ReadModule property. Different images within the file can be accessed using the Frame property. Different portions of the image can be selected using the Selection property. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we open a TIFF file using the XImage object. After we've opened the file we add the image to our document and then save the PDF. [C#] ```csharp using var img = new XImage(); using var doc = new Doc(); img.SetFile(Server.MapPath("../mypics/mypic.jpg")); doc.Rect.Inset(20, 20); doc.AddImageObject(img, false); doc.Save(Server.MapPath("imagesetfile.pdf")); ``` [Visual Basic] ```vbnet Dim theImg As New XImage() Dim doc As New Doc() theImg.SetFile(Server.MapPath("../mypics/mypic.jpg")) doc.Rect.Inset(20, 20) doc.AddImageObject(theImg, False) theImg.Clear() doc.Save(Server.MapPath("imagesetfile.pdf")) doc.Clear() ``` imagesetfile.pdf Also see example code in: ABCpdf Image Example, Doc AddImageObject Function, Doc ColorSpace Property, XImage SetMask Function, XImage Frame Property, XImage Selection Property, XRendering DefaultHalftone Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>