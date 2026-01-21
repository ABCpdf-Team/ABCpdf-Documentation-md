---
title: "01-entryrecipients"
css: "abcpdf-docs.css"
---

|  |  | EntryRecipients Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | Represents the "Recipients" entry of the public-key security handler crypt filter object. | 

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
      
| Represents the "Recipients" entry of the public-key security handler crypt filter object. It is a required entry defined as part of the PDF 1.0 specification. It contains an array which contains strings, representing PDF string objects. If you read the specification you will see that an array of one string may be represented as a single string rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 27, page 69. The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 27, page 91. |  |  | 
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