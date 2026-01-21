---
title: "02-drawpage"
css: "abcpdf-docs.css"
---

|  |  | DrawPage Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Draw the current page from the source to the destination document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int DrawPage() ``` [Visual Basic] ``` Function DrawPage() As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | The ID of the newly added object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Draw the current page from the source PDF document onto the current page of the destination document, returning the ID of the newly added object. The page is scaled to fill the current Rect. It is transformed using the current Transform. Many field and annotation types can only exist as a simple rectangle with sides parallel to the page borders. For this reason you should be cautious about the transforms you use when specifying that annotations should be copied. A transform which involves scale and translation will be fine but one involving rotation and skew factors may result in unusual output if the field or annotation does not support this combination. If you are copying accessibility tags they are taken from the source page and placed into a non structural group. The group is then inserted at the end of the structure for the destination page. In most cases this is what you want. However tagging structures can be complex and not all documents are compatible with each other. If incompatible structures are found the structures in the destination document will be preferred over those from the source document. Pages may be rotated. As such, when drawing one page onto another, you may wish to copy the Page.Rotation from the source page to the destination page. More complex example code to de-rotate a page may be found under the documentation for the Page.Rotation. |  |  | 
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