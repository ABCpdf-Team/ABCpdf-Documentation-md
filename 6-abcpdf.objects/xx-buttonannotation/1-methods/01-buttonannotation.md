---
title: "01-buttonannotation"
css: "abcpdf-docs.css"
---

|  |  | ButtonAnnotation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add button annotation to the current page of the doc. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp ButtonAnnotation(Doc doc, XRect rect, string caption) ``` [Visual Basic] ``` ButtonAnnotation(doc As Doc, rect As XRect, caption As string) ``` |  |  | 
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
| caption | Caption for button | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add button annotation to the current page of the doc. Note that the annotation created using this constructor is meaningless until it is connected with a Field. For this reason you are likely to want to use Doc.Form.AddButton rather than this call. |  |  | 
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