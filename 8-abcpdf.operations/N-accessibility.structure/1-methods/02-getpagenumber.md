---
title: "02-getpagenumber"
css: "abcpdf-docs.css"
---

|  |  | GetPageNumber Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get the page number for a particular page object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int GetPageNumber(Page page) int GetPageNumber(int pageID) ``` [Visual Basic] ``` Sub GetPageNumber(page As Page) As int Sub GetPageNumber(pageID As int) As int ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| page | The Page object. | 
| pageID | The Page IndirectObject ID. | 
| return | The page number. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets the page number for a particular page object. The object can be specified either using a Page object or an IndirectObject ID. The page number is a one based index - the first page is number one. |  |  | 
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