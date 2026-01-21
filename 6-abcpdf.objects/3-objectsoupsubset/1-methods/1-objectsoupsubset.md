---
title: "1-objectsoupsubset"
css: "abcpdf-docs.css"
---

|  |  | ObjectSoupSubset Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Construct an ObjectSoupSubset. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp ObjectSoupSubset(ObjectSoup soup) ``` [Visual Basic] ``` Sub New(soup As ObjectSoup) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| soup | The soup from which objects will be selected. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create an ObjectSoupSubset. An ObjectSoupSubset is specific to a particular ObjectSoup and may only contain IndirectObjects from that soup. For this reason you should specify the soup in question at the point of construction. If later you attempt to add objects from a different soup then an exception will be raised. |  |  | 
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