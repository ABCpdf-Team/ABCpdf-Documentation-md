---
title: "addimagecopy"
css: "abcpdf-docs.css"
---

|  |  | AddImageCopy Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a copy of an existing image in the Doc, to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddImageCopy(int id) ``` [Visual Basic] ``` Function AddImageCopy(id As Integer) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | An existing image object ID to be copied to the page again. | 
| return | The ID of the newly added Image Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a copy of an image which has already been inserted elsewhere in the document. You can use this facility to add commonly used graphics such as watermarks. The raw image data is inserted only once which means that PDF size is greatly reduced. This method only works with raster or bitmap images. So your ID must have been obtained from a previous call to AddImageFile, AddImageData or AddImageObject. The image is scaled to fill the current Rect. It is transformed using the current Transform. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This example shows how to read an existing PDF document and insert a background image into every page. We start by reading our template PDF document and finding out core information we will need to reference each page. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); int count = doc.PageCount; ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) Dim theCount As Integer = doc.PageCount ``` We cycle through the pages inserting images as we go. We set the layer property to ensure that the image gets added in the background rather than on top of existing content. The first time we add an image file. Subsequent times we reference the image ID. This means that we embed only one copy of the image data and simply reference that data from each page. Finally we save the modified PDF. [C#] ```csharp int id = 0; for (int i = 1; i [Visual Basic] ```vbnet Dim theID As Integer = 0 Dim i As Integer = 1 While i Given the following document. sample.pdf - [Page 1] | sample.pdf - [Page 2] | 
| --- | --- |
| sample.pdf - [Page 3] | sample.pdf - [Page 4] | 

And the following image.

![](../../../images/light.jpg)

This is the kind of output you might expect.

| watermark.pdf - [Page 1] | watermark.pdf - [Page 2] | 
| --- | --- |
| watermark.pdf - [Page 3] | watermark.pdf - [Page 4] | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>