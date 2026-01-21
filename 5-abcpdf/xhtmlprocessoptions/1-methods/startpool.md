---
title: "startpool"
css: "abcpdf-docs.css"
---

|  |  | StartPool Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Start the process pool for the HTML Engine. |  |  | 

</td>
  </tr>
  <tr>
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| **[C#]** ```csharp bool StartPool() ``` [Visual Basic] ``` Function StartPool() As Boolean ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr>
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| Name | Description | 
| --- | --- |
| return | Whether the process pool is started anew. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr>
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| This starts the process pool for the HTML Engine (without rendering an HTML page). This method returns false if the process pool has been started before the method is called. |  |  | 
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