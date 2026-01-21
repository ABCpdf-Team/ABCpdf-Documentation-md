---
title: "1-renderoperation"
css: "abcpdf-docs.css"
---

|  |  | RenderOperation Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| RenderOperation Constructor. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp RenderOperation(Doc doc) ``` [Visual Basic] ``` Sub New(doc As Doc) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | The PDF Document | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create a RenderOperation to allow rendering of multiple pages from different threads. You can use Doc.Rendering to set rendering options before creating a RenderOperation. When a RenderOperation is created, relevant doc properties are copied, so modifying properties of Doc.Rendering after creating the operation does not affect the RenderOperation. Likewise, setting the current page to another page after creating the operation has no effect. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Save method. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>