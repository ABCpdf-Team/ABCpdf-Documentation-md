---
title: "01-choicefieldannotation"
css: "abcpdf-docs.css"
---

|  |  | ChoiceFieldAnnotation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add choicefield annotation to the current page of the doc. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp ChoiceFieldAnnotation(Doc doc, XRect rect) ``` [Visual Basic] ``` ChoiceFieldAnnotation(doc As Doc, rect As XRect) ``` |  |  | 
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

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add choicefield annotation to the current page of the doc. Note that the annotation created using this constructor is meaningless until it is connected with a Field. For this reason you are likely to want to use Doc.Form.AddListBoxField or Doc.Form.AddComboBoxField rather than this call. |  |  | 
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