---
title: "getdata"
css: "abcpdf-docs.css"
---

|  |  | GetData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the raw binary content of the stream. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp byte[] GetData() byte[] GetData(bool decompress) ``` [Visual Basic] ``` Function GetData() As Byte() Function GetData(decompress As Boolean) As Byte() ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| decompress | Whether the data should be decompressed. Default false. | 
| return | The raw binary content of the stream. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Get the raw binary content of the stream. This method does not alter the content of the StreamObject so it is an efficient way of getting the data without altering the document. If decompression is requested but could not be performed, then an exception will be raised. This can occur if the source data is corrupt. |  |  | 
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