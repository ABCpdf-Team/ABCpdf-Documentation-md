---
title: "isidentity"
css: "abcpdf-docs.css"
---

|  |  | IsIdentity Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | n/a | Yes | Whether the font is a composite glyph encoded identity font | 

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
      
| Whether the font is a composite glyph encoded identity font. The normal way to identify a character in a font is to use a standard such as ASCII. Language encodings such as Latin work this way. For characters outside this range the PDF format allows you to reference font glyphs directly using the glyph index within the font. This is known as an identity encoding. Language encodings such as Unicode work this way. Identity encodings are very flexible but they do hardwire the document to a particular font file and as such the font must be embdded. Care should be taken when operating on identty encoded embedded font files. |  |  | 
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