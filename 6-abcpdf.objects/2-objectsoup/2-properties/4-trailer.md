---
title: "4-trailer"
css: "abcpdf-docs.css"
---

|  |  | Trailer Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp StreamObject ``` [Visual Basic] `StreamObject` | n/a | Yes | The Trailer or XRef for the document. | 

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
      
| The Trailer or XRef StreamObject for the document. In PDF 1.4 documents have trailer dictionary. In PDF 1.5 documents have XRef streams. Internally ABCpdf only uses XRef streams but - when writing PDF 1.4 documents - it converts the XRef to a standard trailer before output. |  |  | 
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