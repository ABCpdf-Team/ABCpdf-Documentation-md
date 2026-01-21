---
title: "1-maxprocesses"
css: "abcpdf-docs.css"
---

|  |  | MaxProcesses Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | 10 (from registry value HtmlProcessPoolSize) | No | The maximum number of processes for the HTML Engine. | 

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
      
| This specifies the maximum number of processes for the HTML Engine, so the value depends on the selected engine. You can call SkipEngineDependencyCheck to avoid getting an exception for non-application of engine-dependent options. The initial value comes from registry value HtmlProcessPoolSize if the engine supports a variable number of processes. Changes made to the property value affect only the specified engine and are not propagated to the registry. For the MSHtml engine, the property value is always 1 because the out-of-process execution (see registry value MSHtmlBootstrap) only supports 1 process. Attempt to set this property for the MSHtml engine will cause an exception. For the Gecko engine, the property value is fixed after the process pool has started. Attempt to change the property value for the Gecko engine while the process pool has started will cause an exception. For the Chrome engine, the property value specifies the upper bound of the number of processes for creating worker processes. Decreasing the property value below ProcessCount does not terminate existing worker processes. |  |  | 
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