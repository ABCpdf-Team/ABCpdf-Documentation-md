---
title: "3-fromstream"
css: "abcpdf-docs.css"
---

|  |  | FromStream Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Creates an XImage from a Stream. |  |  | 

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| **[C#]** ```csharp static XImage FromStream(Stream stream, XReadOptions options) ``` [Visual Basic] ``` Shared Function FromStream(stream As Stream, options As XReadOptions) As XImage ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Name | Description | 
| --- | --- |
| stream | The stream containing the graphic. | 
| options | The settings for the read. The XImage takes ownership of this parameter. This may be null. | 
| return | The resulting IndirectObject. | 

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| The stream will typically be one of the following types: JPEG, GIF, TIFF, BMP, PNG, PSD, PDB, EXIF, WMF, EMF, EPS, PS or SWF (Flash). For details of additional formats which are supported and the way they are imported, see the ReadModule property and the the Doc.Read method. The advantage of this method over SetStream, is that you can specify the ReadModule you would like to use. This allows precise control over the way that your graphics are imported. In addition you can also control the way that transparency is treated using the PreserveTransparency property. The object takes the ownership of the XReadOptions, which is disposed of when the object is disposed of. You can make the object release the ownership without disposing of the XReadOptions using the parameterized overloads of Dispose and Clear. The XReadOptions must not be modified as long as the object has the ownership. If the returned XImage has the NeedsStream property set to true, you must ensure that the specified stream will remain present and unmodified until the XImage object is cleared, disposed of, or garbage-collected. When this happens the XImage takes ownership of the Stream, which is disposed of when the object is disposed of. You can make the object release the ownership, without disposing of the Stream using the parameterized overloads of Dispose and Clear. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>