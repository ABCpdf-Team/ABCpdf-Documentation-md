---
title: "uri"
css: "abcpdf-docs.css"
---

|  |  | Uri Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | null | No | The URI to the file | 

`may throw Exception()`

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
      
| The URI to the file. For the default plaform, attempting to set this property to a value which is not a valid URI will result in an exception being thrown. To convert a standard Windows path to a URI use (new System.Uri(path).AbsouteUri.For some values of the Platform property (e.g. Mac, DOS, Unix) raw file paths can be used. However these are obsolete and while you may see PDFs which contain them, you would be inadvised to generate new documents containing these structures. |  |  | 
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