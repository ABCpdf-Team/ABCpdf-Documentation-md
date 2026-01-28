# Frame Property

## Notes

Some file formats can contain more than one image. The FrameCount property reflects the number of images.

You can change the currently selected image using the Frame property. As you change the frame the Width, Height, HRes and VRes properties will change to reflect the dimensions and resolution of the currently selected image. When you add an Image using the Doc.AddImageObject method the currently selected frame is added.

Flash (SWF) movies contain a number of frames. You can set the current frame using this property. If you set this property to a negative number it indicates the number of milliseconds (rather than frames) into the movie.

## Example

[C#] using var img = new XImage(); using var doc = new Doc(); img.SetFile("../mypics/multipage.tif"); for (int i = 1; i <= img.FrameCount; i++) { img.Frame = i; doc.Page = doc.AddPage(); doc.AddImageObject(img, false); } doc.Save("imageframe.pdf");

imageframe.pdf - [Page 1]

imageframe.pdf - [Page 2]

