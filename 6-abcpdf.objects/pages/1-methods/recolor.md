---
title: "recolor"
css: "abcpdf-docs.css"
---

|  |  | Recolor Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Converts the pages from one color space to another. |  |  | 

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
      
| Converts the pages from one color space to another. This method calls the Page.Recolor method on all Page objects within this group of pages. |  |  | 
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