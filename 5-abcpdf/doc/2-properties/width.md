# Width Property

## Notes

The width determines the width of lines drawn using methods like AddLine and FrameRect. The width is measured in the current Units.

The AddLine method creates lines centered on the points you provide. This means if you draw a horizontal line with a width of ten the line will extend five points above your start position and five points below it.

The FrameRect method draws lines outside the rectangle you provide. So if you frame a rectangle using a width of ten, the drawn rectangle will extend ten points above, below, to the left and to the right of your specified rectangle. No drawing will fall within the rectangle.

## Example

The following code adds two lines to a document. The first line has a width of ten points and the second has a width of twenty points.

[C#] using var doc = new Doc(); doc.Width = 10; doc.AddLine(10, 10, 300, 300); doc.Width = 20; doc.AddLine(10, 300, 300, 10); doc.Save(Server.MapPath("docwidth.pdf")); [Visual Basic] Using doc As New Doc() doc.Width = 10 doc.AddLine(10, 10, 300, 300) doc.Width = 20 doc.AddLine(10, 300, 300, 10) doc.Save(Server.MapPath("docwidth.pdf")) End Using

docwidth.pdf

Also see example code in: ABCpdf Text Flow Example, ABCpdf Text Flow Round Image Example, ABCpdf Advanced Graphics Example, Doc AddArc Function, Doc AddLine Function, Doc AddOval Function, Doc AddPie Function, Doc AddPoly Function, Doc Options Property, Doc TopDown Property, XColor Components Property, XTransform Skew Function, XTransform Translate Function, ColorSpace Gamma Property, ColorSpace WhitePoint Property, Page GetBitmap Function, ImageOperation GetImageProperties Function.

