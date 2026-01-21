---
title: "encodetext"
css: "abcpdf-docs.css"
---

|  |  | EncodeText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Encode text for use with PDF text operators. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string EncodeText(string text, EncodingSupport support) string EncodeText(string text, EncodingSupport support, out int outCount) ``` [Visual Basic] ``` Function EncodeText(text As String, support As EncodingSupport) Function EncodeText(text As String, support As EncodingSupport, ByRef outCount As Integer) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | The text to be encoded. | 
| support | The way in which characters not included in the font are to be encoded. | 
| outCount | The number of characters in (parameter) text that are encoded in the return value. | 
| return | The PDF string containing the encoded text. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to convert Unicode text into PDF string for use with the Tj or the TJ operator. The EncodingSupport enumeration can take any of the following values: All – encode all text. NoneIfAnyNotSupported – encode nothing if any character is not included in the font. SupportedPrefix – encode up to and excluding the first character not included in the font. Note that the encoding for a font is constructed and cached at the time the font is first created. So changing the encoding for the font will not result in a corresponding change of behavior from this method. If this is something you need to do then you will need to create an entirely new font. |  |  | 
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