---
title: "compression"
css: "abcpdf-docs.css"
---

|  |  | Compression Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp CompressionType ``` [Visual Basic] `CompressionType` | See description. | Yes | The primary compression type. | 

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
      
| A single stream can be compressed and encoded using multiple methods. This property reflects the primary compression type used by the stream. Compression types which result in high levels of compression (e.g. JPEG) are considered more important than those that do not (e.g. ASCII 85). The CompressionType enumeration may take the following values: None Unknown Flate Lzw Ccitt Jpeg Jpx AsciiHex Ascii85 RunLength Jbig2 Crypt More details of these compression types can be found in Section 3.3 of the Adobe PDF Specification. |  |  | 
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