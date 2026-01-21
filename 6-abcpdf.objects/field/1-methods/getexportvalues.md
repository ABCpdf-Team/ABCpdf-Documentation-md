---
title: "getexportvalues"
css: "abcpdf-docs.css"
---

|  |  | GetExportValues Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the export values for this field. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string[] GetExportValues() ``` [Visual Basic] ``` Function GetExportValues() As String() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | An array of strings - one for each option. The size of the array is always equal to the number of Options. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets the export values for this field. Choice fields such as Combo boxes and Lists have a value selected from one of their Options. However it is possible to specify an export value which is different from the value of field. The export value will be used if the form data is exported or submitted in some way so it is purely for external use. This function allows you to get the export values from the field. Please note that export values are only meaningful for fields of FieldType FieldType.Combo or FieldType.List and they are only relevant for form export. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>