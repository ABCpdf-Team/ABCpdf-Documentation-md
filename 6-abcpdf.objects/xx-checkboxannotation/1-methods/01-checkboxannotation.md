---
title: "01-checkboxannotation"
css: "abcpdf-docs.css"
---

|  |  | CheckBoxAnnotation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add checkbox annotation to the current page of the doc. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp CheckBoxAnnotation(Doc doc, XRect rect, bool selected) ``` [Visual Basic] ``` CheckBoxAnnotation(doc As Doc, rect As XRect, selected As bool) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | Doc | 
| rect | Location for the annotation | 
| selected | Whether the checkbox should be checked or not | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add checkbox annotation to the current page of the doc. Note that the annotation created using this constructor is meaningless until it is connected with a Field. For this reason you are likely to want to use Doc.Form.AddCheckbox rather than this call. |  |  | 
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