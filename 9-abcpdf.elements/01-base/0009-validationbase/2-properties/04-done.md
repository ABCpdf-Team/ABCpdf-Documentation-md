---
title: "04-done"
css: "abcpdf-docs.css"
---

|  |  | Done Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp HashSet ``` [Visual Basic] `HashSet` | null | Yes | Gets the set of IDs which have been processed. | 

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
      
| Gets the set of IDs which have been processed. During validation many IndirectObjects will be encountered. Each time this happens, the ID value is added to this property. The result is a set of IDs which allows you to determine the Objects that were validated. If some are not validated this will be generally because they were not referenced anywhere. However it may also be that they were referenced but that the references were not part of the PDF specification and thus could not be followed. |  |  | 
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