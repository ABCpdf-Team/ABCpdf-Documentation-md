---
title: "01-virtualpageoperation"
css: "abcpdf-docs.css"
---

|  |  | VirtualPageOperation Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a VirtualPageOperation. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp VirtualPageOperation(Doc doc) VirtualPageOperation(Doc doc, double width, double height) VirtualPageOperation(Doc doc, XRect rect) ``` [Visual Basic] ``` VirtualPageOperation(doc As Doc) VirtualPageOperation(doc As Doc, width As double, height As double) VirtualPageOperation(doc As Doc, rect As XRect) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| doc | The Doc for which the page is intended. | 
| width | The width of the page in points. | 
| height | The height of the page in points. | 
| rect | The rectangle for the page in points. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create a VirtualPageOperation. If no page dimensions are specified the page will default to the current document MediaBox. Creating this process sets the current Doc.Page to the newly created virtual page. This means you can immediately use Doc methods to add content to this page. However it also means that after you have finished with this object, you will need to set the Doc.Page before you can add content to existing pages of the document. |  |  | 
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