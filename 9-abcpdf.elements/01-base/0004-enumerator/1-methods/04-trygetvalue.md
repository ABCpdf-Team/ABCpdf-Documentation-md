---
title: "04-trygetvalue"
css: "abcpdf-docs.css"
---

|  |  | TryGetValue Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets the value associated with the specified key. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual bool TryGetValue(string key, out value) virtual bool TryGetValue(TKey key, out value) ``` [Visual Basic] ``` Overridable Function TryGetValue(key As string, value As out) As Boolean Overridable Function TryGetValue(key As TKey, value As out) As Boolean ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| key | The key of the value to get. | 
| value | When this method returns this contains the value associated with the specified key. If the key was not found this contains the default value for the type of the value. | 
| return | True if the DictElement contains the specified key otherwise false. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Gets the value associated with the specified key. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>