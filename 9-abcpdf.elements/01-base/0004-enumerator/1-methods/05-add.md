---
title: "05-add"
css: "abcpdf-docs.css"
---

|  |  | Add Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Adds the specified key and value to the dictionary. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void Add(string key, T value) virtual void Add(TKey key, TVal value) ``` [Visual Basic] ``` Overridable Function Add(key As string, value As T) As void Overridable Function Add(key As TKey, value As TVal) As void ``` `ArgumentException: Thrown if the key was already present. NullReferenceException: Thrown if the key or value was null.` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| key | The key of the element to add. | 
| value | The value of the element to add. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Adds the specified key and value to the dictionary. This method adds an item to the dictionary. If the key or value is null then this method will throw an ArgumentNullException. If the key is already present in the dictionary then this method will throw an ArgumentException. |  |  | 
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