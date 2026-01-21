---
title: "subset"
css: "abcpdf-docs.css"
---

|  |  | Subset Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Subset a previously embedded font. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp bool Subset() bool Subset(string characters) bool Subset(int[] glyphs) ``` [Visual Basic] ``` Function Subset() As Boolean Function Subset(characters as String) As Boolean Function Subset(glyphs() As Integer) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| characters | The character set to be used for the subsetting. | 
| glyphs | The set of glyph IDs to be used for the subsetting. | 
| return | Whether subsetting was performed succesfully. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to subset a previously embedded font. Many PDF producers are not efficient at subsetting fonts. Subsetting previously embedded fonts can be a time consuming operation but can also result in a significant reduction in file size. If you provide a character set string then this is a relatively fast operation. However if you do not pass a character set then one has to be constructed and to do this it is necessary to analyze the entire document to determine what characters are being used. In this case if a call to Catalog.AnalyzeContent has not already been made then one will be triggered. This call will subset embedded TrueType and CFF fonts (Compact Font Format). If the font is referenced or if the font is not one of these types then this function will return false. This method operates on a copy-on-write basis so that fonts that share font descriptors will not be affected if one of their siblings is subsetted. The font will remain the same but a new font descriptor will be generated. |  |  | 
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