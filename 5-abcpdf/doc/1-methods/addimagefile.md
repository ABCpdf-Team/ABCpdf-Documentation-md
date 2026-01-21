---
title: "addimagefile"
css: "abcpdf-docs.css"
---

|  |  | AddImageFile Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Extract an image from a file and add it to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| [C#] ``` int AddImageFile(string path) int AddImageFile(string path, int frame) ``` [Visual Basic] ``` Function AddImageFile(path As String) As Integer Function AddImageFile(path As String, frame As Integer) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | A file path, URL or html string to be added to the page. | 
| frame | Some image types support multiple frames or pages. This is the one based index specifying the required frame (default one). | 
| return | The Object ID of the newly added Image Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds an image to the current page returning the ID of the newly added object. This method supports JPEG, JPEG 2000, TIFF, EMF, WMF, PS (PostScript) or EPS (Encapsulated PostScript). Images embedded using this method are inserted using a restricted range of ReadModules. For this reason you may wish to prefer the use of the AddImageObject method. AddImageFile is the equivalent of AddImageObject with the transparent parameter set to true. The only difference between AddImageFile and AddImageObject relates to the treatment of EMF and WMF files. AddImageFile defaults to the EmfVector ReadModule which means that the vector nature of such files will be preserved. AddImageObject defaults to the BasicImage ReadModule which means that such files will be rasterized. For more details see the ReadModule property. The image is scaled to fill the current Rect. It is transformed using the current Transform. Transparency. Occasionally you may find that you need to invert the transparency of your image. To do this you can assign a decode array using the ID returned from this function. To invert the transparency: [C#] ```csharp theDoc.SetInfo(theDoc.GetInfoInt(theID, "XObject"), "/SMask*/Decode", "[1 0]"); ``` [Visual Basic] ```vbnet theDoc.SetInfo(theDoc.GetInfoInt(theID, "XObject"), "/SMask*/Decode", "[1 0]") ``` A similar technique can be used for inverting or altering color levels on the image itself. To invert an RGB image: [C#] ```csharp theDoc.SetInfo(theDoc.GetInfoInt(theID, "XObject"), "/Decode", "[1 0 1 0 1 0]"); ``` [Visual Basic] ```vbnet theDoc.SetInfo(theDoc.GetInfoInt(theID, "XObject"), "/Decode", "[1 0 1 0 1 0]") ``` | 
| --- |

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds an image to the current page positioned at the bottom left. [C#] ```csharp using var doc = new Doc(); doc.Rect.String = "0 0 510 638"; string path = Server.MapPath("../mypics/pic.jpg"); doc.AddImageFile(path, 1); doc.Save(Server.MapPath("docaddimage.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.String = "0 0 510 638" Dim thePath As String = Server.MapPath("../mypics/pic.jpg") doc.AddImageFile(thePath, 1) doc.Save(Server.MapPath("docaddimage.pdf")) End Using ``` docaddimage.pdf Also see example code in: PixMap SetAlpha Function, PixMap ToGrayscale Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>