---
title: "item"
css: "abcpdf-docs.css"
---

|  |  | Item Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets or sets a particular field referenced by full name. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Field this[string name] ``` [Visual Basic]`Default Property Item(name As String) As Field` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| name | The fully qualified name of the field. | 
| return | The matching field. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to retrieve a field referenced by fully qualified name. If no matching field can be found then a null value will be returned. When setting a value any intermediate fields will be created and the provided field name will be updated to reflect the field path provided. In C# this property is the indexer for the class. See the XForm object for details of how fully qualified names are constructed. |  |  | 
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