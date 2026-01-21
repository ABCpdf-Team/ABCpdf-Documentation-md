---
title: "5-revision"
css: "abcpdf-docs.css"
---

|  |  | Revision Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | Yes | The revision of the document in which this object is stored. | 

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
      
| The revision of the document in which this object is stored. PDF documents can be incrementally updated so that changes are appended to the document rather than overwriting the original. This means that it is possible to revert back to a previous version of the document. This feature is mostly used for document signatures so that the act of signing the document does not invalidate previous signatures. Objects from the oldest update will have a Revision of one and and larger values indicate more recent updates. A value of zero indicates that the object was not read from stream. |  |  | 
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