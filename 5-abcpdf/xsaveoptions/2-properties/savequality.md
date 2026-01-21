---
title: "savequality"
css: "abcpdf-docs.css"
---

|  |  | SaveQuality Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 75 | No | The quality for lossy image compression. | 

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
      
| This property determines the quality of output images that use lossy compression in document export. Under some circumstances it may be necessary to decompress JPEG and JPEG 2000 images that are stored in a PDF and to recompress them for output. This typically occurs when exporting to another format which does not support exactly the same features as are supported in PDF. This property specifies the quality for the recompression of such images. This is only used during export to XPS, DOCX, HTML, and WebGL. |  |  | 
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