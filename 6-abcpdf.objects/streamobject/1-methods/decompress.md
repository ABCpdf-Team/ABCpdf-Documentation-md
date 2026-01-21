---
title: "decompress"
css: "abcpdf-docs.css"
---

|  |  | Decompress Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Decompress the data in the stream. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp bool Decompress() ``` [Visual Basic] ``` Function Decompress() As Boolean ``` |  |  | 
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
| return | Whether the data in the stream is uncompressed. | 

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
      
| This method removes all compression from the stream. Under some circumstances it may not be possible to fully decompress the stream. In these situations the function will return false. In occasional and unusual situations, decompression may change the document to a greater extent than one might expect. For example if a PixMap is JPEG 2000 compressed it may contain interleaved transparency. Because interleaved transparency is only permitted in JPEG 2000 images, at the point of decompression the alpha needs to be separated off into a separate PixMap.SMask entry. However this type of situation is uncommon and normally the effects of decompression are limited to the object being decompressed. |  |  | 
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