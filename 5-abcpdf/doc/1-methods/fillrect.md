---
title: "fillrect"
css: "abcpdf-docs.css"
---

|  |  | FillRect Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a painted rectangle to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int FillRect() int FillRect(double radiusX, double radiusY) ``` [Visual Basic] ``` Function FillRect() As Integer Function FillRect(radiusX As Double, radiusY As Double) As Integer ``` |  |  | 
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
| return | The Object ID of the newly added Graphic Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds a painted rectangle to the current page. The rectangle location and size is determined by the current rectangle, the fill color is determined by the current color and any options are determined by the current options. By specifying values for the horizontal and vertical radius parameters you can draw rectangles with rounded corners. The values refer to the radii of the ellipse used to draw the corners. By setting the horizontal radius parameter to half the width of the rect and the vertical radius parameter to half the height of the rect you can draw filled ovals and circles. The FillRect function returns the Object ID of the newly added Graphic Object. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code adds a blue filled rectangle to a document. The frame is inset from the edges of the document by 200 points horizontally and 100 points vertically. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(200, 100); doc.Color.Blue = 255; doc.FillRect(); doc.Save(Server.MapPath("docfillrect.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(200, 100) doc.Color.Blue = 255 doc.FillRect() doc.Save(Server.MapPath("docfillrect.pdf")) End Using ``` docfillrect.pdf Also see example code in: ABCpdf eForm Placeholder Example, ABCpdf Advanced Graphics Example, Doc AddImageBitmap Function, Doc AddImageObject Function, Doc AddXObject Function, Doc Color Property, XHtmlOptions HideBackground Property, XImage SetMask Function, XRendering SaveAlpha Property, Page GetBitmap Function, PixMap SetChromakey Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>