---
title: "regeneratetounicode"
css: "abcpdf-docs.css"
---

|  |  | RegenerateToUnicode Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Attempt to regenerate a ToUnicode map. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool RegenerateToUnicode() ``` [Visual Basic] ``` Function RegenerateToUnicode() As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | Whether a new ToUnicode map was inserted. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Attempt to regenerate a ToUnicode map using embedded font data as a key. Complex fonts are generally embedded using an identity encoding which references characters by glyph index rather than character code. Because glyph indexes are specific to a particular font, to extract text from the PDF you need a table mapping the glyph indexed to character codes. This map is called the ToUnicode map. Well behaved PDF producers will insert a ToUnicode map for all fonts that they embed. However some font producers may fail to do so. This means that copying or extracting text from such a PDF will result in gibberish. In some cases it is possible to regenerate the ToUnicode map from the embedded font data. This function attempts to do so and returns true if a new ToUnicode map was inserted. This function only works on composite fonts and calling it on other types of fonts will not do anything. |  |  | 
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