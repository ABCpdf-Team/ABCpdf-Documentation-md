---
title: "4-clone"
css: "abcpdf-docs.css"
---

|  |  | Clone Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a deep copy of the current IndirectObject. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp IndirectObject Clone() ``` [Visual Basic] ``` Function Clone() As IndirectObject ``` |  |  | 
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
| return | The newly created copy. | 

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
      
| This function creates a new object that is a copy of this instance. The copy is a deep copy and all contained objects are copied as part of the clone process. The copy is not associated with any ObjectSoup. Note that many methods require that an object be part of a soup. For this reason it is quite common to call doc.ObjectSoup.Add with the newly cloned object before calling methods on it. If at a later date the object needs to be deleted this can be done using ObjectSoup.Remove. |  |  | 
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