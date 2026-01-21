---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | XImage Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Allows access to images stored in files or in data. XImages can be added to a document using the Doc.AddImageObject method. ``` System.Object WebSupergoo.ABCpdf13.XImage Implements: IDisposable ``` |  |  | 

</TD></TR> 
<TR> <TD vAlign=top>&nbsp;</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 
| Method | Description | 
| --- | --- |
| S» FromFile | Creates an XImage from a file path. | 
| S» FromData | Creates an XImage from an array of bytes. | 
| S» FromStream | Creates an XImage from a Stream. | 
| Dispose | Dispose of the object. | 
| Clear | Clears the image. | 
| SetData | Load an image from data. | 
| SetFile | Load an image from a file. | 
| SetMask | Assign a soft mask to the image. | 
| SetStream | Load an image from stream. | 
| GetInfo | Gets internal information from the image. | 

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD vAlign=top>&nbsp; </TD><TD width=14>&nbsp;</TD><TD vAlign=top> 
| Property | Description | 
| --- | --- |
| AppliedOrientation | The orientation transform that should be applied to the image. | 
| BoundingBox | The physical bounds of the image in points. | 
| Frame | The currently selected frame. | 
| FrameCount | The number of frames in the image. | 
| FrameRate | The default frame rate for a moving image. | 
| HasRealRes | Whether the image specifies the resolution. | 
| Height | The height of the current frame (pixels). | 
| HRes | The horizontal resolution of the current frame (DPI). | 
| Indirect | Whether the image will be added using indirect mode. | 
| NeedsFile | Whether the file needs to exist. | 
| NeedsStream | Whether the stream needs be kept open. | 
| Orientation | The orientation of the current frame. | 
| Selection | The current selection rectangle. | 
| Type | The type of image. | 
| VRes | The vertical resolution of the current frame (DPI). | 
| Width | The width of the current frame (pixels). | 

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR> 
<TR> <TD>&nbsp; </TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>