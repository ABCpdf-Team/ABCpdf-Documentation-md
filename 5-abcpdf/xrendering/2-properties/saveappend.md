---
title: "saveappend"
css: "abcpdf-docs.css"
---

|  |  | SaveAppend Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to append to (rather than overwrite) existing image files. | 

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
      
| This property determines whether the Save method appends to (rather than overwrites) existing image files. If this property is set to true and a file already exists then the Save method appends the rendered image to the exisiing file rather than just overwriting it. In this way you can build up multi-page images. For in-memory operations you can use this property set to true in conjunction with a MemoryStream and the Save overload that supports streams. This property is used for TIFF output only. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the SaveCompression property. Also see example code in: XRendering SaveCompression Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>