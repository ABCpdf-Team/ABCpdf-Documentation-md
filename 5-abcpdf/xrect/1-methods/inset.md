---
title: "inset"
css: "abcpdf-docs.css"
---

|  |  | Inset Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Insets the edges of the rectangle. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Inset(double x, double y) ``` [Visual Basic] ``` Sub Inset(x As Double, y As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| x | The amount to inset the left and right edges. | 
| y | The amount to inset the top and bottom edges. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Insets the edges of the rectangle by a specified horizontal and vertical amount. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code. [C#] ```csharp var rc = new XRect(); rc.String = "0 0 200 100"; Response.Write($"Rect = {rc}"); Response.Write(""); rc.Inset(10, 20); Response.Write("Inset = " + rc.String); ``` [Visual Basic] ```vbnet Dim rc As New XRect() rc.String = "0 0 200 100" Response.Write($"Rect = {rc}") Response.Write("") rc.Inset(10, 20) Response.Write("Inset = " + rc.String) ``` Produces the following output. Rect = 0 0 200 100Inset = 10 20 190 80 Also see example code in: ABCpdf Text Flow Example, ABCpdf Text Flow Round Image Example, ABCpdf Multistyle Example, ABCpdf Landscape Example, ABCpdf Small Table Example, ABCpdf Large Table Example, ABCpdf Paged HTML Example, ABCpdf eForm FDF Example, Doc AddColorSpaceFile Function, Doc AddColorSpaceSpot Function, Doc AddImageBitmap Function, Doc AddImageDoc Function, Doc AddImageToChain Function, Doc AddOval Function, Doc AddPie Function, Doc AddXObject Function, Doc FillRect Function, Doc FrameRect Function, Doc ColorSpace Property, Doc Rect Property, Doc String Property, Doc TextStyle Property, XColor Alpha Property, XColor Components Property, XHtmlOptions GetTagRects Function, XHtmlOptions LinkDestinations Method, XHtmlOptions LinkPages Method, XHtmlOptions HtmlCallback Property, XImage SetData Function, XImage SetFile Function, XImage SetMask Function, XImage SetStream Function, XImage Selection Property, XRendering AntiAliasImages Property, XRendering AntiAliasText Property, XRendering IccCmyk Property, XTextStyle Bold Property, XTextStyle HPos Property, XTextStyle Indent Property, XTextStyle Italic Property, XTextStyle Justification Property, XTextStyle Kerning Property, XTextStyle ParaSpacing Property, XTextStyle Strike Property, XTextStyle Strike2 Property, XTextStyle Underline Property, XTextStyle VPos Property, XTransform Magnify Function, XTransform Reset Function, ColorSpace Gamma Property, ColorSpace WhitePoint Property, Page GetBitmap Function, PixMap SetChromakey Function, ArrayAtom FromContentStream Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>