---
title: "flags"
css: "abcpdf-docs.css"
---

|  |  | Flags Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp FontFlags ``` [Visual Basic] `FontFlags` | n/a | No | The Font Descriptor Flags entry | 

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
      
| The Font Descriptor Flags entry. The FontFlags type is a flags type enumeration so the different values can be combined together using bitwise operations. It may take the following values: FixedPitch (All glyphs have the same width; as opposed to proportional or variable-pitch fonts, which have different widths) Serif (Glyphs have serifs - short strokes drawn at an angle on the top and bottom of glyph stems. Sans serif fonts do not have serifs) Symbolic (Font contains glyphs outside the Adobe standard Latin character set. This flag and the Nonsymbolic flag are mutually exclusive) Script (Glyphs look like cursive handwriting) Nonsymbolic (Font uses the Adobe standard Latin character set or a subset of it) Italic (Glyphs have slanted dominant vertical strokes) AllCap (Font contains no lowercase letters) SmallCap (Lower case letters in this font look like smaller versions of their upper case equivalents) ForceBold (Whether bold glyphs shall be painted with extra pixels even at very small text sizes) The flags detailed here are descriptive. So reading them from an existent font object will provide information on the style. However changing them will not necessarily change it. If the font is referenced then the viewing application will need to find an appropriate system font and it should try to take account of these flags. However if the fonts is embedded then changing the flags will not change the underlying embedded font. Make sure you understand these concepts before you change these values. How do I manipulate flags enumerations? To check a flag you can write code of the following form: [C#] ```csharp bool isSymbolic = font.Flags.HasFlag(FontObject.FontFlags.Symbolic); ``` [Visual Basic] ```vbnet Dim isSymbolic As Boolean = font.Flags.HasFlag(FontObject.FontFlags.Symbolic) ``` To set the flag: [C#] ```csharp font.Flags \|= FontObject.FontFlags.Symbolic; ``` [Visual Basic] ```vbnet font.Flags = font.Flags Or FontObject.FontFlags.Symbolic ``` To clear the flag: [C#] ```csharp font.Flags &= !FontObject.FontFlags.Symbolic; ``` [Visual Basic] ```vbnet font.Flags = font.Flags And Not FontObject.FontFlags.Symbolic ``` | 
| --- |

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
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