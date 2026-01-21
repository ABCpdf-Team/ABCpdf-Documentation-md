---
title: "6-revisioneofs"
css: "abcpdf-docs.css"
---

|  |  | RevisionEOFs Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp long[] ``` [Visual Basic] `long[]` | n/a | Yes | This provides the end of trailer offsets within the underlying PDF stream. | 

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
      
| This provides the end of trailer offsets within the underlying PDF stream. These correspond with the length of each revision. The offset is the number of bytes to the start of the %%EOF tag rather than to the end of the physical file. The %%EOF tag is a line so normally, but not always, it will be followed by a CR, LF or CRLF. By truncating the original PDF file to the end of this line you can recreate the PDF at that revision. |  |  | 
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