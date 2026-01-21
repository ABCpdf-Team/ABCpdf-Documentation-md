---
title: "addimage"
css: "abcpdf-docs.css"
---

|  |  | AddImage Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds an image to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddImage(XImage image) int AddImage(string path) int AddImage(byte[] data) int AddImage(string path, int page) int AddImage(byte[] data, int page) int AddImage(int id) int AddImage(System.Drawing.Bitmap bm) int AddImage(Doc doc, int page) int AddImage(Doc doc, int page, XRect src) ``` [Visual Basic] ``` Function AddImage(image As XImage) As Integer Function AddImage(path As String) As Integer Function AddImage(data() As Byte) As Integer Function AddImage(path As String, page As Integer) As Integer Function AddImage(data() As Byte, page As Integer) As Integer Function AddImage(id As Integer) As Integer Function AddImage(bm As System.Drawing.Bitmap) As Integer Function AddImage(doc As Doc, page As Integer) As Integer Function AddImage(doc As Doc, page As Integer, src As XRect) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| image | An XImage containing the image to be added to the page. | 
| path | A file path, URL or html string to be added to the page. | 
| data | The raw JPEG data to be added to the page. | 
| id | An existing image object ID to be copied to the page again. | 
| bm | A .NET Bitmap to be added to the page. | 
| doc | A PDF document page to be added to the page. | 
| page | The page of the document to be added. | 
| src | The source area of the document page to be added. | 
| return | The ID of the newly added Image Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds an image to the current page returning the ID of the newly added object. This method attempts to make a sensible decision as to which of the following methods to call dependent on the content of the ImageSpec. AddImageFile AddImageData AddImageCopy AddImageUrl AddImageHtml AddImageToChain AddImageDoc AddImageObject AddImageBitmap This function is provided for backwards compatibility purposes. You should call the appropriate method directly rather than working via this method. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: ABCpdf Text Flow Round Image Example, XRendering ColorSpace Property, XRendering DefaultHalftone Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>