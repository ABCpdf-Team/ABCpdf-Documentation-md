---
title: "03-add"
css: "abcpdf-docs.css"
---

|  |  | Add Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds a Bookmark to the end of the list. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int Add(Bookmark bookmark) int Add(string title) ``` [Visual Basic] ``` Function Add(bookmark As Bookmark) As Integer Function Add(title As String) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| bookmark | The bookmark to be added. | 
| title | The title for the bookmark to be added. | 
| return | The position in which the new element was inserted. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method adds an item to the end of the list. You can add a Bookmark directly or you can use one of the overloaded operators to add a bookmark with a specified title. When you add a string this is encapsulated within a new Bookmark which is then inserted. Bookmarks can exist in only one place at a time. If the Bookmark supplied is already contained by another object then a Clone of the Bookmark is added. |  |  | 
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