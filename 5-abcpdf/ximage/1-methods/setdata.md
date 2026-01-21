---
title: "setdata"
css: "abcpdf-docs.css"
---

|  |  | SetData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Load an image from data. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetData(byte[] data) ``` [Visual Basic] ``` Sub SetData(data() As Byte) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| data | The data containing the graphic. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Load an image from data. The data is expected to be provided as an array of bytes. The data can be any of the following types: JPEG, GIF, TIFF, BMP, PNG, PSD, PDB, EXIF, WMF, EMF, EPS, PS or SWF (Flash). Ultimately each import goes through a ReadModule so for details of additional formats supported and the way they are imported, see the ReadModule property. Different images within the file can be accessed using the Frame property. Different portions of the image can be selected using the Selection property. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Here we read a TIFF file and present the data to the XImage object. We then add the image to our document and then save the PDF. [C#] ```csharp using var img = new XImage(); using var doc = new Doc(); // read the data from a file string path = Server.MapPath("../mypics/mypic.jpg"); using var stream = File.OpenRead(path); byte[] theData = new byte[stream.Length]; stream.Read(theData, 0, (int)stream.Length); // place the data into the image img.SetData(theData); doc.Rect.Inset(20, 20); doc.AddImageObject(img, false); doc.Save(Server.MapPath("imagesetdata.pdf")); ``` [Visual Basic] ```vbnet Dim theImg As New XImage() Dim doc As New Doc() ' read the data from a file Dim thePath As String = Server.MapPath("../mypics/mypic.jpg") Dim theStream As FileStream = File.OpenRead(thePath) Dim theData As Byte() = New Byte(theStream.Length - 1) {} theStream.Read(theData, 0, DirectCast(theStream.Length, Integer)) theStream.Close() ' place the data into the image theImg.SetData(theData) doc.Rect.Inset(20, 20) doc.AddImageObject(theImg, False) theImg.Clear() doc.Save(Server.MapPath("imagesetdata.pdf")) doc.Clear() ``` imagesetdata.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>