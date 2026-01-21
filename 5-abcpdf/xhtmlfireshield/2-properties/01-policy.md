---
title: "01-policy"
css: "abcpdf-docs.css"
---

|  |  | Policy Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Enforcement ``` [Visual Basic] `Enforcement` | Enforcement.None | No | File access enforcement for the worker process | 

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
      
| File access enforcement for the worker process. This property allows you to specify the type of action that should be taken if the HTML engine attempts to access a resource to which it is not allowed. You can choose from the following options: None - No enforcement of the access rules. Do not log any file paths.Deny - Prohibit access if the rules do not specify that access should be allowed. Always report an error if this happens. Log the file path via the Log property.Mask - Prohibit access if the rules do not specify that access should be allowed. Attempt to continue the operation without error. Do not log the file path. Log - If the rules do not specify that access should be allowed, allow it, but also log the file path via the Log property. |  |  | 
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