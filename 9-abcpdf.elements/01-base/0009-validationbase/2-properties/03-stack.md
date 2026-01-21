---
title: "03-stack"
css: "abcpdf-docs.css"
---

|  |  | Stack Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp StackValidationStackNode> ``` [Visual Basic] `StackValidationStackNode>` | null | No | Gets or sets the stack. | 

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
      
| Gets or sets the stack. Validation is a recursive process. One Element validates each of its child Elements. Each of those in turn validate their children. In the event that an inconsistency is found, it useful to know how the current Element was arrived at. This property allows you to examine the current state of the stack including all parent StackNodes up to the root. There may be apparent duplicates on the stack as sub-classes may result in multiple calls to the Start function. For this reason, for a stack trace, you will generally want to use the GetStackTrace function. However you may also find that you want to Peek at the top - current - item for added detail when reporting errors. |  |  | 
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