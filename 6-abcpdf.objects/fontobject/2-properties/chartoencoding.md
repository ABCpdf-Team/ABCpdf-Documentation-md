---
title: "chartoencoding"
css: "abcpdf-docs.css"
---

|  |  | CharToEncoding Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IDictionary ``` [Visual Basic] `IDictionary` | n/a | Yes | The Unicode to glyph mapping table for all the characters in the font | 

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
      
| The Unicode to glyph mapping table for all the characters in the font. In this context, the glyph value is the value which occurs in the content stream when using this font. While the encoding used is often similar to ASCII, it may vary cionsiderably depending on the way the font has been included in the PDF. To map from the glyph encoding to a Unicode character see EncodingToChar. |  |  | 
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