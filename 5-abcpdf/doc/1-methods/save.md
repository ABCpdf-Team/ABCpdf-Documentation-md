---
title: "save"
css: "abcpdf-docs.css"
---

|  |  | Save Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Saves the document as PDF. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Save(string path) void Save(Stream stream) ``` [Visual Basic] ``` Sub Save(path As String) Sub Save(stream As Stream) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| path | The destination file path. | 
| stream | The destination stream. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to export the current document as PDF, XPS, PostScript, HTML, DOCX, WebGL or SWF. To export as XPS, PostScript, DOCX or HTML you need to specify a file path with an appropriate extension - ".xps", ".ps", ".docx", ".htm", ".html" or ".swf". If the file extension is unrecognized then the default PDF format will be used. When saving to a Stream the format can be indicated using a Doc.SaveOptions.FileExtension property such as ".htm" or ".xps". For HTML you must provide a sensible value for the Doc.SaveOptions.Folder property. For XPS streams must be both readable and writable - FileAccess.ReadWrite and not simply FileAccess.Write. ABCpdf operates an intelligent just-in-time object loading scheme which ensures that only those objects that are required are loaded into memory. This means that if you are modifying large documents then server load will be kept to a minimum. The original PDF document must be available for as long as the Doc object is being used. As a result you cannot modify or overwrite a PDF file while it is read into a Doc object. You will need to save your PDF to another location and then swap the two files around after the Doc object's use of the PDF is ended (with a call to Clear, Dispose, or Read with another PDF file). If you need to obtain a PDF as raw data you can use the GetData function. The SaveOptions.Refactor setting determines whether duplicate and redundant objects are eliminated when the document is saved. Versions. ABCpdf automatically determines the version depending on the features you use. If you use features from only the 1.1 specification it will write a 1.1 PDF. If you use 1.3 features it will write a 1.3 PDF. If you use 1.4 features it will write a 1.4 PDF. Ditto 1.5 and 1.6. If you're using a PDF template or drawing from another PDF the final output will be the minimum version used in these templates. In many real world applications this will be the factor which determines the version in the final output produced by ABCpdf. There is no advantage in producing a 1.6 document if you're not using features from the 1.6 feature set. To do this will simply stop users of older versions of Acrobat from accessing a document which should be available to them. | 
| --- |

When saving to SWF, if the [Doc.SaveOptions.Template](../../xsaveoptions/2-properties/template.md) is null, the current page is exported with [Rect](../2-properties/rect.md) as the bounds of the Flash movie using [Doc.SaveOptions.TemplateData.MeasureDpiX](../../xsavetemplatedata/2-properties/measuredpix.md) and [Doc.SaveOptions.TemplateData.MeasureDpiY](../../xsavetemplatedata/2-properties/measuredpiy.md) if specified. Otherwise, [Doc.SaveOptions.Template](../../xsaveoptions/2-properties/template.md) specifies the path to a SWF file. The saved SWF file starts with the template SWF files, and a frame is added for each page in the document. The script added is in ActionScript 2. If the template's version is Flash Player 7 or lower, the saved file's version will be Flash Player 8. For information on the interaction between the added frames and the script from the template, please refer to the example Flash file. Images are output in JPEG if (1) they are in DeviceGray or DeviceRGB and already in JPEG (without any other compression on top), or (2) they are not in the indexed color space and both the width and the height are at least 8 pixels. For (1), the original JPEG data is used so you can control the quality by pre-compressing the images; for (2), the output will use 80% quality.

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code illustrates how one might add text to a PDF and then save it out. [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; doc.AddText("Hello World"); doc.Save(Server.MapPath("docsave.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 doc.AddText("Hello World") doc.Save(Server.MapPath("docsave.pdf")) End Using ``` docsave.pdf Also see example code in: ABCpdf Text Flow Example, ABCpdf Text Flow Round Image Example, ABCpdf Multistyle Example, ABCpdf Image Example, ABCpdf Deletion Example, ABCpdf Headers and Footers Example, ABCpdf Landscape Example, ABCpdf Small Table Example, ABCpdf Large Table Example, ABCpdf Unicode Example, ABCpdf Paged HTML Example, ABCpdf eForm Fields Example, ABCpdf eForm Placeholder Example, ABCpdf eForm Stamp Example, ABCpdf eForm FDF Example, ABCpdf Advanced Graphics Example, ABCpdf Fields, Markup and Movies Example, ABCpdf WPF Tables Example, Doc AddArc Function, Doc AddBookmark Function, Doc AddColorSpaceFile Function, Doc AddColorSpaceSpot Function, Doc AddFont Function, Doc AddGrid Function, Doc AddImageBitmap Function, Doc AddImageCopy Function, Doc AddImageDoc Function, Doc AddImageFile Function, Doc AddImageObject Function, Doc AddImageToChain Function, Doc AddImageUrl Function, Doc AddLine Function, Doc AddObject Function, Doc AddOval Function, Doc AddPage Function, Doc AddPie Function, Doc AddPoly Function, Doc AddText Function, Doc AddTextStyled Function, Doc AddXObject Function, Doc Append Function, Doc Delete Function, Doc EmbedFont Function, Doc FillRect Function, Doc FrameRect Function, Doc Read Function, Doc RemapPages Method, Doc SetInfo Function, Doc Color Property, Doc ColorSpace Property, Doc Encryption Property, Doc Font Property, Doc FontSize Property, Doc MediaBox Property, Doc Options Property, Doc Page Property, Doc Pos Property, Doc Rect Property, Doc String Property, Doc TextStyle Property, Doc TopDown Property, Doc Transform Property, Doc Width Property, XColor Alpha Property, XColor Components Property, XEncryption SetCryptMethods Function, XHtmlOptions GetTagRects Function, XHtmlOptions LinkDestinations Method, XHtmlOptions LinkPages Method, XHtmlOptions ForChrome Property, XHtmlOptions ForGecko Property, XHtmlOptions ForMSHtml Property, XHtmlOptions ForWebKit Property, XHtmlOptions AddForms Property, XHtmlOptions BrowserWidth Property, XHtmlOptions HideBackground Property, XHtmlOptions HtmlCallback Property, XHtmlOptions HtmlEmbedCallback Property, XHtmlOptions HttpAdditionalHeaders Property, XHtmlOptions ImageQuality Property, XHtmlOptions LogonName Property, XHtmlOptions RetryCount Property, XHtmlOptions UseScript Property, XImage SetData Function, XImage SetFile Function, XImage SetMask Function, XImage SetStream Function, XImage Frame Property, XImage Selection Property, XPoint Point Property, XRect Rectangle Property, XSaveOptions Template Property, XSaveOptions WritePageSeparator Property, XSaveTemplateData SetMeasureResolution Function, XTextStyle Bold Property, XTextStyle CharSpacing Property, XTextStyle HPos Property, XTextStyle Indent Property, XTextStyle Italic Property, XTextStyle Justification Property, XTextStyle Kerning Property, XTextStyle LeftMargin Property, XTextStyle LineSpacing Property, XTextStyle Outline Property, XTextStyle ParaSpacing Property, XTextStyle Size Property, XTextStyle Strike Property, XTextStyle Strike2 Property, XTextStyle Underline Property, XTextStyle VPos Property, XTextStyle WordSpacing Property, XTransform Invert Function, XTransform Magnify Function, XTransform Reset Function, XTransform Rotate Function, XTransform Skew Function, XTransform Translate Function, XTransform AngleUnit Property, Catalog Metadata Property, ColorSpace Gamma Property, ColorSpace WhitePoint Property, FileSpecification FileSpecification Function, FontObject Widths Property, Page GetBitmap Function, Page MakeFormXObject Function, Page VectorizeText Function, Page Rotation Property, Page Thumbnail Property, PixMap Recolor Function, PixMap Resize Function, PixMap SetAlpha Function, PixMap SetChromakey Function, PixMap ToGrayscale Function, Signature AddLTV Function, Signature Sign Method, Signature Validate Function, Signature CompliancePades Property, Signature CustomSigner Property, Signature CustomSigner2 Property, ArrayAtom FromContentStream Function, OpAtom Find Function, ProcessingInfo FrameNumber Property, RecolorOperation Recolor Function, RecolorOperation IccCmyk Property, XpsImportOperation Import Function, SwfImportOperation Import Function, TextOperation Group Function, ImageOperation GetImageProperties Function, FlattenTransparencyOperation Flatten Function, ReduceSizeOperation Compact Function, AccessibilityOperation AccessibilityOperation Constructor, VectorizeTextOperation Vectorize Method, CloudVisionOperation StartOcr Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>