---
title: "rect"
css: "abcpdf-docs.css"
---

|  |  | Rect Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp XRect ``` [Visual Basic] `XRect` | The dimensions of the current page. | No | The current rectangle used for drawing operations. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property determines the current rectangle. This is used by a number of operations including AddText, AddImage, FrameRect and FillRect. The XRect object represents a rectangular area in two-dimensional space. The properties of the XRect object represent the bottom left and top right corners of the area. AddText adds text within the current rectangle wrapping the text at the edges. The AddImage methods add an image scaled to fill the current rectangle. FrameRect frames the current rectangle and FillRect fills the current rectangle. When you change this property the Pos property is reset to point to the top left of the Rect. XRect is a class not a struct. Unlike System.Drawing Rectangle and RectangleF the XRect is a class rather than a struct. This means that variables are passed by reference rather than value - you may have more than one reference to the same object. As such you need to be careful not to over share. For example the following is wrong, ```csharp theDoc.Rect = theDoc.MediaBox; // incorrect ``` The reason it is incorrect is because you are now sharing one rectangle between two properties - if you change the Rect you also change the MediaBox. Suppose you change the Rect, add some text, then add a new page. Because the Rect has changed, the MediaBox has also changed, and when you add a new page it will likely be the wrong size. Instead you want something more like one of these, ```csharp theDoc.Rect = theDoc.MediaBox.Clone(); // correcttheDoc.Rect.String = theDoc.MediaBox.String; // also correct ``` | 
| --- |

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code creates a PDF document containing a number of concentric frames. [C#] ```csharp using var doc = new Doc(); doc.Rect.String = "50 50 550 550"; for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.String = "50 50 550 550" Dim i As Integer = 1 While i docrect.pdfAlso see example code in: ABCpdf Text Flow Example, ABCpdf Text Flow Round Image Example, ABCpdf Multistyle Example, ABCpdf Image Example, ABCpdf Headers and Footers Example, ABCpdf Landscape Example, ABCpdf Small Table Example, ABCpdf Large Table Example, ABCpdf Paged HTML Example, ABCpdf eForm Placeholder Example, ABCpdf eForm FDF Example, ABCpdf Advanced Graphics Example, ABCpdf PDF Rendering Example, Doc AddColorSpaceFile Function, Doc AddColorSpaceSpot Function, Doc AddImageBitmap Function, Doc AddImageDoc Function, Doc AddImageFile Function, Doc AddImageObject Function, Doc AddImageToChain Function, Doc AddOval Function, Doc AddPie Function, Doc AddXObject Function, Doc FillRect Function, Doc FrameRect Function, Doc ColorSpace Property, Doc String Property, Doc TextStyle Property, Doc TopDown Property, Doc Transform Property, XColor Alpha Property, XColor Components Property, XHtmlOptions GetTagRects Function, XHtmlOptions LinkDestinations Method, XHtmlOptions LinkPages Method, XHtmlOptions HtmlCallback Property, XImage SetData Function, XImage SetFile Function, XImage SetMask Function, XImage SetStream Function, XImage Selection Property, XRect Rectangle Property, XRendering AntiAliasImages Property, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering ColorSpace Property, XRendering DefaultHalftone Property, XRendering DrawAnnotations Property, XRendering IccCmyk Property, XRendering SaveCompression Property, XTextStyle Bold Property, XTextStyle CharSpacing Property, XTextStyle HPos Property, XTextStyle Indent Property, XTextStyle Italic Property, XTextStyle Justification Property, XTextStyle Kerning Property, XTextStyle LeftMargin Property, XTextStyle LineSpacing Property, XTextStyle Outline Property, XTextStyle ParaSpacing Property, XTextStyle Strike Property, XTextStyle Strike2 Property, XTextStyle Underline Property, XTextStyle VPos Property, XTextStyle WordSpacing Property, XTransform Invert Function, XTransform Magnify Function, XTransform Reset Function, XTransform Skew Function, XTransform Translate Function, ColorSpace Gamma Property, ColorSpace WhitePoint Property, FontObject Widths Property, Page GetBitmap Function, Page Rotation Property, PixMap SetAlpha Function, PixMap SetChromakey Function, PixMap ToGrayscale Function, ArrayAtom FromContentStream Function, XpsImportOperation Import Function, SwfImportOperation Import Function, TextOperation Group Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>