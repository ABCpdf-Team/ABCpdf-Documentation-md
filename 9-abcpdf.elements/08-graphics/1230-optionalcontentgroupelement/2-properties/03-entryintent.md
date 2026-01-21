---
title: "03-entryintent"
css: "abcpdf-docs.css"
---

|  |  | EntryIntent Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | Represents the "Intent" entry of the optional content group dictionary object. | 

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
      
| Represents the "Intent" entry of the optional content group dictionary object. It is an optional entry defined as part of the PDF 1.0 specification. It contains an array which contains strings, representing PDF name objects. The PDF specification states that items in this array assume a value of "View" if no value has been provided. Items in this array may take one of the following valid values:. ViewDesign. If you read the specification you will see that an array of one string may be represented as a single string rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 98, page 222. The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 96, page 274. |  |  | 
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