---
title: "deinline"
css: "abcpdf-docs.css"
---

|  |  | DeInline Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Makes any inline images into external images. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void DeInline(bool convertAnnotations) void DeInline(bool convertAnnotations, out PixMap[] detachedPixMaps) ``` [Visual Basic] ``` Sub DeInline(convertAnnotations As Boolean) Sub DeInline(convertAnnotations As Boolean, ByRef detachedPixMaps As PixMap()) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| convertAnnotations | Whether to convert the color space of annotation appearance streams. | 
| detachedPixMaps | All the PixMaps which were extracted as a result of the call. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Makes any inline images into external images. Images in PDF documents are generally held as external object and are then referenced from the page content stream. However it is also possible to inline small images and embed the binary image data directly into the PDF content stream. This is not always desirable as it complicates certain types of PDF processing. This method allows you to extract such inline images and convert them into standard external PixMap objects. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
|  |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>