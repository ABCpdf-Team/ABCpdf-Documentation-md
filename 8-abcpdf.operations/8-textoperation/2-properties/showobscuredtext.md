---
title: "showobscuredtext"
css: "abcpdf-docs.css"
---

|  |  | ShowObscuredText Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to show overlapping repeated text content. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Whether to show overlapping repeated text content. Overlapping repeated text content is most typically used for a synthetic bold effect. While the multiple copies of the text provide an appropriate bold-like look, they are not semantically valid since they appear as one unit. In cases where you are looking at the semantic meaning of the text, you typically only want the initial text item. However if you are replacing text then you may wish to include all the text items so that when you change one you also change the others. Using this setting you control whether you want this text returned by GetText. |  |  | 
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