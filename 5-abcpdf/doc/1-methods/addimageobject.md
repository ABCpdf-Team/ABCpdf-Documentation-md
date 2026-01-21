---
title: "addimageobject"
css: "abcpdf-docs.css"
---

|  |  | AddImageObject Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds an XImage based image to the current page. |  |  | 

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| [C#] ```csharp int AddImageObject(XImage image) int AddImageObject(XImage image, bool transparent) ``` [Visual Basic] ```vbnet Function AddImageObject(image As XImage) As Integer Function AddImageObject(image As XImage, transparent As Boolean) As Integer ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Name | Description | 
| --- | --- |
| image | An XImage containing the image to be added to the page. | 
| transparent | Whether transparency information should be preserved. This parameter overrides the PreserveTransparency property of the XReadOptions used to create the XImage. If this parameter is not specified and the XImage has been created without a XReadOptions, this parameter is defaulted to false. | 
| return | The ID of the newly added Image Object. If the image is added as multiple objects, such as if it has been created with an XReadOptions with ReadModule of SwfVector (with a non-null Operation), Xps, or XpsAny, the ID is zero. If XReadOptions.Operation has been null, the temporary SwfImportOperation allows this method to return the ID of the GraphicLayer for the frame of XReadOptions.Frame. | 

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| If the XImage has been created with an XReadOptions with ReadModule that uses an Operation, the operation will be invoked and the result depends on the operation. Otherwise, this method gets an image from the Image object and adds it to the current page returning the ID of the newly added object.Adds the Selection of the current Frame returning the ID of the newly added object. Ultimately each image which is imported goes through a ReadModule, so see that property for the types of images that can be imported and how they are handled. If the Transparent parameter is set to true then any transparency information will be preserved. This allows you to add formats such as transparent GIF, PNG with alpha channel, or images with masks set using the Image.SetMask method.The image is scaled to fill the current Rect. It is transformed using the current Transform. Hyperlinks. Sometimes you may wish to insert annotations such as links to an external web page specified using a URI or URL. The AddTextStyled method allows you to specify links but only on text. If, for example, you want to insert a link over content such as an image you need to add it separately. You can do this using code of the following form. [C#] ```csharp static int AddLinkToUri(Doc doc, XRect rect, string uri) { int id = doc.AddObject("> /Border [0 0 0] >>"); doc.SetInfo(doc.Page, "/Annots*[]:Ref", id); doc.SetInfo(id, "/Rect:Rect", doc.Rect.String); doc.SetInfo(id, "/A/URI:Text", uri); return id; } ``` [Visual Basic] ```vbnet Private Shared Function AddLinkToUri(ByVal doc As Doc, ByVal rect As XRect, ByVal uri As String) As Integer Dim id As Integer = doc.AddObject("> /Border [0 0 0] >>") doc.SetInfo(doc.Page, "/Annots*[]:Ref", id) doc.SetInfo(id, "/Rect:Rect", doc.Rect.String) doc.SetInfo(id, "/A/URI:Text", uri) Return id End Function ``` If you wish to link to a particular page specified by page ID you can use code of the following form. [C#] ```csharp static int AddLinkToPage(Doc doc, XRect rect, int pageID) { int id = doc.AddObject("> >>"); doc.SetInfo(doc.Page, "/Annots*[]:Ref", id); doc.SetInfo(id, "/Rect:Rect", doc.Rect.String); doc.SetInfo(id, "/A/D[0]:Ref", pageID.ToString()); return id; } ``` [Visual Basic] ```vbnet Private Shared Function AddLinkToPage(ByVal doc As Doc, ByVal rect As XRect, ByVal pageID As Integer) As Integer Dim id As Integer = doc.AddObject("> >>") doc.SetInfo(doc.Page, "/Annots*[]:Ref", id) doc.SetInfo(id, "/Rect:Rect", doc.Rect.String) doc.SetInfo(id, "/A/D[0]:Ref", pageID.ToString()) Return id End Function ``` | 
| --- |

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| The following code adds a transparent GIF against a gray background.[C#] ```csharp using var img = new XImage(); img.SetFile(Server.MapPath("../mypics/mypic.gif")); using Doc doc = new Doc(); doc.Color.String = "200 200 200"; doc.FillRect(); doc.Rect.String = "0 0 480 640"; doc.AddImageObject(img, true); doc.Save(Server.MapPath("docaddimageobject.pdf")); ``` [Visual Basic] ```vbnet Dim theImg As New XImage() theImg.SetFile(Server.MapPath("../mypics/mypic.gif")) Dim doc As New Doc() doc.Color.String = "200 200 200" doc.FillRect() doc.Rect.String = "0 0 480 640" doc.AddImageObject(theImg, True) theImg.Clear() doc.Save(Server.MapPath("docaddimageobject.pdf")) doc.Clear() ``` docaddimageobject.pdfAlso see example code in: ABCpdf Image Example, XImage SetData Function, XImage SetFile Function, XImage SetMask Function, XImage SetStream Function, XImage Frame Property, XImage Selection Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>