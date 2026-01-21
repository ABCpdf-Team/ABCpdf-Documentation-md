---
title: "06-entryfdecodeparms"
css: "abcpdf-docs.css"
---

|  |  | EntryFDecodeParms Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp ArrayElementParameterElement> ``` [Visual Basic] `ArrayElementParameterElement>` | null | No | Represents the "FDecodeParms" entry of the stream object. | 

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
      
| Represents the "FDecodeParms" entry of the stream object. It is an optional entry defined as part of the PDF 1.2 specification. It contains an array which contains ParameterElements. If you read the specification you will see that an array of one ParameterElement may be represented as a single ParameterElement rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 5, page 20. The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 5, page 32. |  |  | 
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