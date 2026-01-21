---
title: "embedfont"
css: "abcpdf-docs.css"
---

|  |  | EmbedFont Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Search for and embed a font file into this font object |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool EmbedFont() ``` [Visual Basic] ``` Function EmbedFont() As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | Whether the font was embedded successfully. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Search for and embed a font file into this font object. If an existing font file is already embedded it will be replaced. If you wish to subset the font you will need to call the Subset method after embedding the font. Calling this function on Identity encoded fonts should be done with great caution as these types of fonts rely on glyph indexes and are thus specific to a particular font file. |  |  | 
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