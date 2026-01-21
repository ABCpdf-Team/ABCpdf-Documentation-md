---
title: "07-insert"
css: "abcpdf-docs.css"
---

|  |  | Insert Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Inserts a Bookmark into the list at the specified position. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Insert(int index, Bookmark bookmark) void Insert(int index, string title) ``` [Visual Basic] ``` Sub Insert(index As Integer, bookmark As Bookmark) Sub Insert(index As Integer, title As String) ``` `may throw ArgumentOutOfRangeException()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| index | The zero-based index at which value should be inserted. | 
| bookmark | The bookmark to be added. | 
| title | The title for the bookmark to be added. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Inserts an item into the list at the specified position. You can insert a Bookmark directly or you can use one of the overloaded operators to insert a bookmark with a specified title. When you insert a string this is encapsulated within a new Bookmark which is then inserted. Bookmarks can exist in only one place at a time. If the Bookmark supplied is already contained by another object then a Clone of the Bookmark is added. If the index equals the number of items in the array then the bookmark is appended to the end. If the index is not a valid index this method throws an ArgumentOutOfRangeException. |  |  | 
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