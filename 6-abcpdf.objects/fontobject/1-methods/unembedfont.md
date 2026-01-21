---
title: "unembedfont"
css: "abcpdf-docs.css"
---

|  |  | UnembedFont Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Unembed the font if this is a simple operation. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int UnembedSimpleFont() ``` [Visual Basic] `UnembedSimpleFont() As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | The number of bytes of font data that were removed as a result of this call. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Unembed the font if this is a simple operation. Latin based fonts can often be unembedded as a simple and fast operation. However Unicode and symbolic fonts are more complex to unembed and cannot be simply removed from the document. To unembed a composite font you need to use the ReduceSizeOperation class. This function returns the number of bytes of font data that were removed as a result of this call. Note that it is possible for multiple font objects to reference the same embedded font. In this case each call to unembed will return the same number and the actual font will only actually be removed from the document if all references to it are released. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>