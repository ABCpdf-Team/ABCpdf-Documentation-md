---
title: "7-getdocobjectid"
css: "abcpdf-docs.css"
---

|  |  | GetDocObjectID Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the object ID of the IndirectObject in the PDF document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int GetDocObjectID() ``` [Visual Basic]`Function GetDocObjectID() As Integer` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | The object ID (or zero if it has no associated object). | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The method returns the object ID of the IndirectObject for this JavaScript value. For example, if this value is a Field, the method returns the object ID of the corresponding Annotation. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the JSOptions.SetUp event. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>