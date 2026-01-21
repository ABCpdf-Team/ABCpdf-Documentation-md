---
title: "embeddedfile"
css: "abcpdf-docs.css"
---

|  |  | EmbeddedFile Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp EmbeddedFile ``` [Visual Basic] `EmbeddedFile` | null | No | The embedded file if one has been embedded in the PDF | 

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
      
| The embedded file if one has been embedded in the PDF.If a file has not been embedded then the URL needs to be intepreted in the context of the current PDF to locate the external file.Setting this property will clear the EmbeddedFiles property if one is present. This property requires reference to other objects in the ObjectSoup. If this object is not part of an ObjectSoup this property will always be null. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Also see example code in: FileSpecification FileSpecification Function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>