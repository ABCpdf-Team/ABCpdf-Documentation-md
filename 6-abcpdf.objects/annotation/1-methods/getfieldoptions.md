---
title: "getfieldoptions"
css: "abcpdf-docs.css"
---

|  |  | GetFieldOptions Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| The field options for any form field associated with this annotation. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp string[] GetFieldOptions() ``` [Visual Basic] ``` Function GetFieldOptions() As String() ``` |  |  | 
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
| return | The list of field options. | 

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
      
| This function gets the field options for any form field associated with this annotation. Typically you assign a value using the FieldValue. Some fields such as Text fields will accept any value. Others such as Checkboxes and List Boxes accept only a limited range of options. You can obtain these options using this method. The unmarked state of a Checkbox or Radio Button is always "Off". The marked state varies and is available via this function. This function will always return a one item arrray for this type of field. The set of options for a Combo Box or List Box is available via this property. This function will return as many items as there are possible values. Pushbuttons, Signatures and Text fields do not have options. |  |  | 
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