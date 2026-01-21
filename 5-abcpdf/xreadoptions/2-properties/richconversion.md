---
title: "richconversion"
css: "abcpdf-docs.css"
---

|  |  | RichConversion Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether rich conversion should be performed. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </tbody></table>
    </td>
  </tr>
  <tr> 
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property determines whether rich conversion is performed. Set to true to convert document text fields, popup comments, file links and bookmarks to their PDF equivalent. While this produces a better output for documents containing these features, it can impact the speed of conversion for some large documents, in particular for those containing large table-of-contents. If you do not need these features you may prefer to set it to false. At present this setting is only relevant for the conversion of DOC and DOCX files using MS Word. |  |  | 
| --- | --- | --- |

</td>
  </tr>
    <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR>
</tbody></table>