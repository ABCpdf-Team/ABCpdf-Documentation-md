---
title: "getcontentdata"
css: "abcpdf-docs.css"
---

|  |  | GetContentData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the decompressed content data from the page. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp byte[] GetContentData() byte[] GetContentData(StreamObject[] contents) ``` [Visual Basic] ``` Function GetContentData() As Byte() Sub GetContentData(contents As StreamObject{}) As Byte() ``` |  |  | 
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
| contents | The content streams from which to get the data. If null is passed all the Page content streams will be used. | 
| return | The content data. | 

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
      
| Gets the decompressed content data from the page. If the page contains multiple content streams then the data from these will be concatenated so you can treat them as one. However, while the data is concatenated, the streams are left untouched - the function does not alter the page. If a content stream could not be decompressed then an exception will be raised. If you need to go through all the content streams associated with a set of pages, the ContentStreamOperation class provides this type of functionality. |  |  | 
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