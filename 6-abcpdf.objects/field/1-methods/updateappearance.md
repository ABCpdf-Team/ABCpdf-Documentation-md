---
title: "updateappearance"
css: "abcpdf-docs.css"
---

|  |  | UpdateAppearance Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Update the appearance of all the Annotations associated with this field |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void UpdateAppearance() ``` [Visual Basic] ``` Sub UpdateAppearance() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| none | n/a | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Update the appearance of all the Annotations associated with this field. A field may have more than one appearance on one or more pages. Each appearance is represented as an Annotation. When a field is changed in a way which may impact the visual rendition on the page, the appearance of all the Annotations associated with that field need to be updated. When you update the Value this happens automatically. However if you change other properties such as the TextColor you will need to make an explicit call to ensure the appearance streams are updated. |  |  | 
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