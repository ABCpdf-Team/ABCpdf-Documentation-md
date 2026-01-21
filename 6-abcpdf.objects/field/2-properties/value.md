---
title: "value"
css: "abcpdf-docs.css"
---

|  |  | Value Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "" | No | The field value. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader" width="64">![](../../../images/steel-pin.gif)  

      Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top" width="739"> 
      
| This property allows you access to the value of the field. You may wish to assign or query the form field value using this property. Text fields have a free-text value. Checkboxes and Radio Buttons have a value which is either "Off" or the on-state of the control as specified in the Options. Combo Boxes and List Boxes have values restricted to a set of selections as specified in the Options property. Pushbuttons and Signatures do not have a value. Some fields are associated with JavaScript which may be used for validation or formatting. In the case that you assign a value which causes an exception in the JavaScript, that exception will be propagated up the chain and will cause a corresponding C# exception to be raised. If you do not want to run such script, set the Doc.Form.UseFieldScript property to false. Common Operations. Set the value of a text field: [C#] ```csharp theField.Value = "Mr Jones"; ``` [Visual Basic] ```vbnet theField.Value = "Mr Jones" ``` Set a checkbox: [C#] ```csharp theField.Value = theField.Options[0]; ``` [Visual Basic] ```vbnet theField.Value = theField.Options(0) ``` Clear a checkbox: [C#] ```csharp theField.Value = "Off"; ``` [Visual Basic] ```vbnet theField.Value = "Off" ``` Set the fifth Radio Button in a group: [C#] ```csharp theField.Value = theField.Options[4]; ``` [Visual Basic] ```vbnet theField.Value = theField.Options(4) ``` | 
| --- |

| Multiline Form Fields Tip. When inserting carriage returns into multiline form fields use carriage returns (\r) only. Using line feeds (\n) or a carriage return linefeed combination (\r\n) is less compatible with older versions of Acrobat. | 
| --- |

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader" width="64">![](../../../images/steel-pin.gif)  

      Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top" width="739"> 
      
| Also see example code in: ABCpdf eForm Fields Example. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>