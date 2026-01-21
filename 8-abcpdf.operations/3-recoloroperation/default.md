# RecolorOperation Class

An operation used to recolor PDF documents.

``` System.Object WebSupergoo.ABCpdf13.Operations.Operation WebSupergoo.ABCpdf13.Operations.RecolorOperation ```

## Method Description RecolorOperation RecolorOperation Constructor. &nbsp;Recolor Recolor pages in a document. GetPipe Gets a color conversion pipe which may be used to map colors from one color space to another. &nbsp; inherited methods... &nbsp;

## Property Description IccRgb The path to the default RGB ICC color profile. IccGray The path to the default Gray ICC color profile. IccCmyk The path to the default CMYK ICC color profile. IccOutput The path to the default output ICC color profile. ConvertAnnotations Gets or sets a value indicating whether annotations are to be recolored. DestinationColorSpace Gets or sets the destination ColorSpace. PreserveK Switch for preserving black options when converting color values to cmyk. PreserveKOptions Tell the color management system how to preserve black when converting color values to cmyk. RenderingIntent Gets or sets the default rendering intent. AllowIntentChanges Whether content in the PDF is allowed to override the rendering intent. Type0SampleCount Gets or sets the number of Type 0 function samples to generate when converting from Type 2 functions. &nbsp; inherited properties...