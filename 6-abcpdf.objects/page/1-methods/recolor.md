---
title: "recolor"
css: "abcpdf-docs.css"
---

|  |  | Recolor Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Converts the page from one color space to another. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Recolor(ColorSpace space, bool convertAnnotations) void Recolor(ColorSpace space, bool convertAnnotations, out PixMap[] recoloredPixMaps) ``` [Visual Basic] ``` Sub Recolor(space As ColorSpace, convertAnnotations As Boolean) Sub Recolor(space As ColorSpace, convertAnnotations As Boolean, ByRef recoloredPixMaps As PixMap()) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| space | The destination color space. | 
| convertAnnotations | Whether to convert the color space of annotation appearance streams. | 
| recoloredPixMaps | All the PixMaps which were recolored as a result of the call. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Converts the page from one color space to another. All images used on the page are converted to the new color space. All color operators used in the page content stream are converted to the new color space. Annotations and fields are not part of the page but instead float over the page. You can choose whether to convert the appearance stream of any annotations or leave them in their native color space. Colors can only be sensibly mapped from one color space to another if we know something about the characteristics of the color space. If your color spaces do not contain this information (e.g. if they are device color spaces) then ABCpdf will use a default color profile. An exception will be thrown if the operation is not possible. This may happen if the Page is not in an ObjectSoup or if the ColorSpace object is in some way invalid. As part of the Recolor process it is necessary to call PixMap.Recolor on all the images used on the page. After the Recolor process has been completed these PixMap objects will no longer be compressed. You may wish to compress them using the StreamObject.Compress method. |  |  | 
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