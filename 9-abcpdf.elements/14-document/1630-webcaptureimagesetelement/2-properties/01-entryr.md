---
title: "01-entryr"
css: "abcpdf-docs.css"
---

|  |  | EntryR Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | Represents the "R" entry of the web capture image set object. | 

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
      
| Represents the "R" entry of the web capture image set object. It is a required entry defined as part of the PDF 1.0 specification. It contains an array which contains integers, representing PDF numeric objects. If you read the specification you will see that an array of one integer may be represented as a single integer rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 354, page 622. The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 390, page 802. |  |  | 
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