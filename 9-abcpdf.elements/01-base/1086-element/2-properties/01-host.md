---
title: "01-host"
css: "abcpdf-docs.css"
---

|  |  | Host Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IndirectObject ``` [Visual Basic] `IndirectObject` | null | Yes | Gets the host IndirectObject. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Gets the host IndirectObject. The host is specified during construction or in a later call to Assign. The host is primarily used to indicate the document to which the Element belongs. As such it can be any IndirectObject in the document. However it is often useful to choose one which is closely associated with the Atom provided. For example, if you create an Element from an IndirectObject, the Host can be itself. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>