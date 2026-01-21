---
title: "vettext"
css: "abcpdf-docs.css"
---

|  |  | VetText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Make a string of text safe for use in a specified encoding. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string VetText(LanguageType type, bool vertical, string text) string VetText(LanguageType type, bool vertical, string text, Func substitute) ``` [Visual Basic] ``` Function VetText(type As LanguageType, vertical As Bool, text As String) As String Function VetText(type As LanguageType, vertical As Bool, text As String, substitute as Func) As String ``` `may throw Exception()` |  |  | 
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
| text | The text to vet. | 
| substitute | A function taking a character and returning a substitute character. | 
| return | The vetted text. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Make a string of text safe for use in a specified encoding. Any characters which are not present in the encoding will be substituted with ones that are. You can optionally specify a function to do the character substitution. If your substitution function returns a character which is not present in the encoding an exception will be raised. |  |  | 
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