---
title: "encodingtochar"
css: "abcpdf-docs.css"
---

|  |  | EncodingToChar Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IDictionary ``` [Visual Basic] `IDictionary` | 0? | No? | The glyph to Unicode mapping table for all the characters in the font | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The glyph to Unicode mapping table for all the characters in the font. In this context, the glyph value is the value which occurs in the content stream when using this font. While the encoding used is often similar to ASCII it may vary cionsiderably depending on the way the font has been included in the PDF. Typically you would use the StringAtom Decode or DecodeDoubleByte methods to allow text operator parameters to be decoded into the base text encoding. These can then be passed through the FontObject EncodingToChar and EncodingToString properties to allow mapping from the text encoding through to Unicode values. To map from a Unicode character to the glyph encoding see CharToEncoding. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>