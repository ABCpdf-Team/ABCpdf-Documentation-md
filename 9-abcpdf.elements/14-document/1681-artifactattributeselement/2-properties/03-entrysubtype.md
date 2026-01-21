---
title: "03-entrysubtype"
css: "abcpdf-docs.css"
---

|  |  | EntrySubtype Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `string` | null | No | Represents the "Subtype" entry of the artifact attributes object. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Represents the "Subtype" entry of the artifact attributes object. It is an optional entry defined as part of the PDF 2.0 specification. It contains a string representing a PDF name object. If provided, this item must always take the value "Header". The specification defines this as exensible which means that it may contain entries in addition to those defined in the specification. In fact almost all objects are extensible but the fact that it is explicitly mentioned, implies that extra entries should be regarded as normal rather than exceptional. For further details see The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: Annex E, page 673.. For definitive details see:. The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 385, page 787. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>