---
title: "framerect"
css: "abcpdf-docs.css"
---

|  |  | FrameRect Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a rectangular frame to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int FrameRect() int FrameRect(bool inside) int FrameRect(double radiusX, double radiusY) int FrameRect(double radiusX, double radiusY, bool inside) ``` [Visual Basic] ``` Function FrameRect() As Integer Function FrameRect(inside As Boolean) As Integer Function FrameRect(radiusX As Double, radiusY As Double) As Integer Function FrameRect(radiusX As Double, radiusY As Double, inside As Boolean) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| radiusX | The horizontal radius to use for rounded corners. | 
| radiusY | The vertical radius to use for rounded corners. | 
| inside | Whether to draw the frame inside the rectangle. | 
| return | The Object ID of the newly added Graphic Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a rectangular frame to the current page. The frame location and size is determined by the current rectangle, the line color is determined by the current color, the line width is determined by the current width and any options are determined by the current options. By specifying values for the horizontal and vertical radius parameters you can draw rectangles with rounded corners. The values refers to the radii of the ellipse used to draw the corners. By setting the horizontal radius parameter to half the width of the rect and the vertical radius parameter to half the height of the rect you can draw ovals and circles. By default frames are drawn round the outside of the current rectangle. This allows you to add content and then frame it ensuring that the frame and the content do not overlap. However sometimes you may wish to draw the frame round the inside of the rectangle. You can do this by setting the inside parameter to true. The FrameRect function returns the Object ID of the newly added Graphic Object. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds a black frame to a document. The frame is inset from the edges of the document by 50 points horizontally and 100 points vertically. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(50, 100); doc.FrameRect(); doc.Save(Server.MapPath("docframerect.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(50, 100) doc.FrameRect() doc.Save(Server.MapPath("docframerect.pdf")) End Using ``` docframerect.pdfAlso see example code in: ABCpdf Text Flow Example, ABCpdf Text Flow Round Image Example, ABCpdf Multistyle Example, ABCpdf Headers and Footers Example, ABCpdf Paged HTML Example, Doc AddImageDoc Function, Doc AddImageToChain Function, Doc Rect Property, Doc Transform Property, XHtmlOptions GetTagRects Function, XHtmlOptions UseScript Property, XRect Rectangle Property, XTextStyle HPos Property, XTextStyle VPos Property, XTransform Magnify Function, XTransform Reset Function, XTransform Skew Function, XTransform Translate Function, FontObject Widths Property, XpsImportOperation Import Function, TextOperation Group Function, ImageOperation GetImageProperties Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>