---
title: "clearcacheddecompressed"
css: "abcpdf-docs.css"
---

|  |  | ClearCachedDecompressed Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Clear the cached, decompressed data for the stream. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void ClearCachedDecompressed() ``` [Visual Basic] ``` Sub ClearCachedDecompressed() ``` |  |  | 
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
| none |  | 

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
      
| The uncompressed data are retrieved from compressed streams during most operations, but the streams are still compressed. The uncompressed data are sometimes cached so that later operations (including the actual decompression of the streams) need not invoke the decompression algorithm. This increases the memory usage, and it is not desirable if the document is to be kept in memory for an extended period of time. This method discards the cached, decompressed data so that a re-read of the document is not required to release the memory. You can apply the effect to multiple stream objects using Doc.ClearCachedDecompressedStreams. |  |  | 
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