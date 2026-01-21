---
title: "fontbbox"
css: "abcpdf-docs.css"
---

|  |  | FontBBox Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XRect ``` [Visual Basic] `XRect` | n/a | Yes | The bounding box for the glyphs in this font | 

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
      
| The bounding box for the glyphs in this font. This XRect corresponds to the xMin, xMax, yMin and yMax entries in the 'head' TrueType table. The PDF format only supports a limited range of metrics so FontObjects read from PDF may contain some approximations compared with 'live' FontObjects which have been added using the Doc.AddFont or Doc.EmbedFont methods. |  |  | 
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