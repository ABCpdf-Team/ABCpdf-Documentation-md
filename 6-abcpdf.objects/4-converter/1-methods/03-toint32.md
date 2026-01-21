---
title: "03-toint32"
css: "abcpdf-docs.css"
---

|  |  | ToInt32 Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Attempts to get an int from the specified entry in a DictAtom or ArrayAtom resolving any references as necessary. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual int? ToInt32(Atom atom, int index) virtual int? ToInt32(Atom atom, string key) virtual int? ToInt32(Atom atom) ``` [Visual Basic] ``` Overridable Function ToInt32(atom As Atom, index As int) As Integer? Overridable Function ToInt32(atom As Atom, key As string) As Integer? Overridable Function ToInt32(atom As Atom) As Integer? ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The DictAtom or ArrayAtom from which to obtain the value. | 
| index | The zero based index from which the value should be obtained. | 
| key | The key identifying the entry to be obtained. | 
| return | The value. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Attempts to get an int from the specified atom resolving any references as necessary. If the simple overload is used then the atom provided must resolve to a value of the correct type. If not then the return value will be null. If a key is provided then the atom must resolve to a DictAtom and the entry in the DictAtom must resolve to a value of the correct type. If this is not the case or the key is null, then the return value will be null. If an index is provided then the atom must resolve to an ArrayAtom and the indexed entry in the ArrayAtom must resolve to a value of the correct type. If this is not the case or if the index is not available, then the return value will be null. |  |  | 
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