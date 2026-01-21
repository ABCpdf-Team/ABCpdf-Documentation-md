---
title: "getpagearrayall"
css: "abcpdf-docs.css"
---

|  |  | GetPageArrayAll Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets all the Page objects under this node and descendents of this node. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp Page[] GetPageArrayAll() ``` [Visual Basic] ``` Function GetPageArrayAll() As Page() ``` |  |  | 
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
| return | An array of Page objects. | 

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
      
| Gets all the Page objects under this node and descendents of this node. The pages are returned in order of page number. The Page.ID can be assigned directly to the Doc.Page property to set the focus to a particular page. For large or badly structured documents it is likely to be faster to use this type of operation than it is to repeatedly access the Doc.PageNumber property. For an array of the immediate children of this node see GetPageArray. |  |  | 
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