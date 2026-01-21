---
title: "01-contentstreamscanner"
css: "abcpdf-docs.css"
---

|  |  | ContentStreamScanner Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a new ContentStreamScanner. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp ContentStreamScanner() ContentStreamScanner(ContentStreamScanner sibling) ``` [Visual Basic] ``` ContentStreamScanner() ContentStreamScanner(sibling As ContentStreamScanner) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| sibling | A scanner which contains cached data. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create a new ContentStreamScanner. A ContentStreamScanner will cache useful resources as they are needed. If you are creating multiple ContentStreamScanners for the same document you can share this cache to increase efficiency. To share cached data in this way pass in a sibling scanner previously used to scan a content stream in the same doc. |  |  | 
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