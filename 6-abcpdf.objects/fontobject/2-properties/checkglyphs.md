---
title: "checkglyphs"
css: "abcpdf-docs.css"
---

|  |  | CheckGlyphs Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to exclude invalid glyphs from our lookup tables | 

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
      
| Whether to exclude invalid glyphs from our lookup tables. When fonts are subsetted the glyphs in the tables may be rendered invalid because they are not used. The encoding continues to exist but the information required to draw the glyphs has been lost. As such it is not a good idea to attempt to use these glyphs even though they may appear to be part of the font. By default we attempt to detect such glyphs and exclude them from any operations or font properties such as the EncodingToChar and CharToEncoding mappings. This prevents them being used inadvertently. |  |  | 
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