---
title: "decodedoublebyte"
css: "abcpdf-docs.css"
---

|  |  | DecodeDoubleByte Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Decode a double byte PDF encoded string into a plain string format |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp StringBuilder DecodeDoubleByte(string text, StringBuilder builder) ``` [Visual Basic] ``` Function DecodeDoubleByte(text As String, builder As StringBuilder) As StringBuilder ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | The text to be decoded. | 
| builder | The StringBuilder to which the encoded representation should be appended. If null then one will be created. | 
| return | The StringBuilder supplied or created. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Decode a double byte PDF encoded string into a plain string format. This may be necessary if you are looking at a content stream using a Composite font with a double byte CMap. This type of operation can be useful if you are extracting text from a PDF content stream containing raw PDF string operators. Typically you would use the StringAtom Decode or DecodeDoubleByte methods to allow text operator parameters to be decoded into the base text encoding. These can then be passed through the FontObject EncodingToChar and EncodingToString properties to allow mapping from the text encoding through to Unicode values. |  |  | 
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