---
title: "getencoding"
css: "abcpdf-docs.css"
---

|  |  | GetEncoding Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Obtain a standard encoding dictionary for use with PDF text operators. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static Dictionary GetEncoding(LanguageType type, bool vertical) ``` [Visual Basic] `Shared Function GetEncoding(type As LanguageType, vertical As Boolean) As Dictionary(Of Char, Char)` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| type | The language type for the desired encoding. | 
| vertical | Whether the writing direction should be horizontal or vertical. | 
| return | A dictionary mapping Unicode values to native character IDs. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to obtain a standard encoding dictionary for use with PDF text operators. Note that the encoding dictionary is defined purely by the language and direction provided as arguments to this function. It is your responsibility to ensure that the returned encoding dictionary is only used with fonts that already have this encoding. If instead you need to encode text using the font encoding specific to this particular font see the EncodeText method. Since the Unicode LanguageType is already Unicode the encoding for this type is identity. For this reason an exception will be thrown if an encoding for this type is requested. See the Fonts and Languages section for details on language types. |  |  | 
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