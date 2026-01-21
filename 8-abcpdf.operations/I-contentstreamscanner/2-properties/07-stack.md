---
title: "07-stack"
css: "abcpdf-docs.css"
---

|  |  | Stack Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp StackGraphicsState> ``` [Visual Basic] `StateGraphicsState>` | n/a | No | The current graphics stack. | 

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
      
| The current graphics stack. This broadly corresponds with the 'Graphics Stack' as described in the PDF Specification. The current graphics stack is what is saved and restored using the PDF save and restore operators. A save pushes a copy of the current state onto the stack. A restore pops the top from the stack. The top item on the stack is available via the State property. |  |  | 
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