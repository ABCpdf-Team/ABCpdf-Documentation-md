---
title: "3-convert"
css: "abcpdf-docs.css"
---

|  |  | Convert Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Converter ``` [Visual Basic] `Converter` | n/a | Yes | A Converter for the document. | 

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
      
| A Converter for the document. The Converter can be used for the resolution and extraction of atomic data held within the document. Because the Converter has direct access to the raw data it can be significantly faster than resolving Atoms directly. This is especially the case for accessing collections such as arrays or dictionaries of data. It is very simple to use. For example to get all the character widths from a font you might use code of the following form. [C#] ```csharp Atom atom = Atom.GetItem(font.Atom, "Widths"); double[] widths = doc.ObjectSoup.Convert.ToDoubleArray(atom, 1000); ``` [Visual Basic] ```vbnet Dim atom As Atom = Atom.GetItem(font.Atom, "Widths") Dim widths As Double() = doc.ObjectSoup.Convert.ToDoubleArray(atom, 1000) ``` |  |  | 
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