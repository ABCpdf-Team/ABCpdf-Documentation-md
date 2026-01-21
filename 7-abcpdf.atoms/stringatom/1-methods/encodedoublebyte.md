---
title: "encodedoublebyte"
css: "abcpdf-docs.css"
---

|  |  | EncodeDoubleByte Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Encode a string into a format for use in a content stream using a composite font with a double byte CMap. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp static StringBuilder EncodeDoubleByte(string text, IDictionary encoding, StringBuilder builder) ``` [Visual Basic] `Shared Function EncodeDoubleByte(text As String, encoding As IDictionary, builder As StringBuilder) As StringBuilder` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| text | The text to be encoded. | 
| encoding | The encoding to use - typically obtained from the FontObject.GetEncoding method. | 
| builder | The StringBuilder to which the encoded representation should be appended. | 
| return | The updated StringBuilder. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Encode a string into a format for use in a content stream using a composite font with a double byte CMap. Typically you will obtain an appropriate encoding from the FontObject.GetEncoding method. This method supports eight bit characters only as this is what is supported by simple fonts. Most commonly you will want to use a Korean, Japanese, ChineseS or ChineseT encoding in either horizontal or vertical format. This method should only be used with composite fonts that specify this type of encoding as only these fonts will understand the fact that the characters are multi-byte. If you attempt to use this method with a simple font then you will get extra characters inserted since each double byte entry will be interpreted as two single characters. See the Fonts and Languages section for details on language types. |  |  | 
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