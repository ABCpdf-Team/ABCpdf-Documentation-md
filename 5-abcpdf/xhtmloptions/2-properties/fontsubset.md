---
title: "fontsubset"
css: "abcpdf-docs.css"
---

|  |  | FontSubset Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether embedded fonts should be subsetted or not. | 

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
      
| This property determines whether embedded fonts are subset. HTML rendering may require that fonts are added to the PDF document. By default these fonts are - where possible - referenced. You can use FontEmbed to ensure that fonts are embedded. When FontEmbed is set to true, you can then use this property to specify if fonts should be subset (only required glyphs are embedded) or not (entire font is embedded). This will considerably increase output size and processing time. |  |  | 
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