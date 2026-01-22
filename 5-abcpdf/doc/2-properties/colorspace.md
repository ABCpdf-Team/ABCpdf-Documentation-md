# ColorSpace Property

## Notes

The current color space.

The ColorSpace is used when the Color is of a matching type. If the color type does not match then the default - device - color space is used.

For example you add a CMYK color space and assign it to the ColorSpace property. All CMYK Colors you use will be defined in terms of this color space. However RGB and Grayscale colors will continue to be defined in terms of the default - device - color spaces.

To get a ColorSpace ID you need to add your color space to the current document using the AddColorSpaceFile or AddColorSpaceSpot method.

## Example

The following code shows how to colorize an image. It adds a base image to the current page and converts it to grayscale. Then it creates a new spot color space and assigns the new color space to the image.

[C#] using var doc = new Doc(); doc.Rect.Inset(20, 20); using var img = new XImage(); img.SetFile(Server.MapPath("../mypics/mypic.jpg")); int id = doc.AddImageObject(img, false); id = doc.GetInfoInt(id, "XObject"); doc.SetInfo(id, "Grayscale", ""); int theCS = doc.AddColorSpaceSpot("MAGENTA", "0 100 0 0"); doc.SetInfo(id, "/ColorSpace:Ref", theCS.ToString()); doc.SetInfo(id, "/Decode", "[1 0]"); doc.Save(Server.MapPath("doccolorspace.pdf")); [Visual Basic] Using doc As New Doc() doc.Rect.Inset(20, 20) Dim theImg As New XImage() theImg.SetFile(Server.MapPath("../mypics/mypic.jpg")) Dim theID As Integer = doc.AddImageObject(theImg, False) theID = doc.GetInfoInt(theID, "XObject") doc.SetInfo(theID, "Grayscale", "") Dim theCS As Integer = doc.AddColorSpaceSpot("MAGENTA", "0 100 0 0") doc.SetInfo(theID, "/ColorSpace:Ref", theCS.ToString()) doc.SetInfo(theID, "/Decode", "[1 0]") doc.Save(Server.MapPath("doccolorspace.pdf")) End Using

doccolorspace.pdf

Also see example code in: Doc AddColorSpaceFile Function, Doc AddColorSpaceSpot Function, XColor Components Property, ColorSpace Gamma Property, ColorSpace WhitePoint Property.

