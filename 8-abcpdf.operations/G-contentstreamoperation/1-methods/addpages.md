---
title: "addpages"
css: "abcpdf-docs.css"
---

|  |  | AddPages Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add and scan selected pages from the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void AddPages() void AddPages(int pageNumber) void AddPages(int startPageNumber, int endPageNumber) void AddPages(int pageNumber, StreamObject[] layers) ``` [Visual Basic] ``` Sub AddPages() Sub AddPages(pageNumber As Integer) Sub AddPages(startPageNumber As Integer, endPageNumber As Integer) Sub AddPages(pageNumber As Integer, layers as StreamObject()) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| pageNumber | The number of the page to be processed. This is a one based index. | 
| startPageNumber | The number of the first page to be processed. This is a one based index. | 
| endPageNumber | The number of the last page to be processed. This is a one based index. | 
| layers | The layers to be scanned. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add and scan selected pages from the document. If no arguments are supplied then all pages will be added. |  |  | 
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