---
title: "1-defineproperties"
css: "abcpdf-docs.css"
---

|  |  | DefineProperties Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Defines a list of this object's own properties. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void DefineProperties(IEnumerable> props) ``` [Visual Basic]`Sub DefineProperties(props As IEnumerable(Of KeyValuePair(Of String, Object)))` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| props | A list of name-value pairs of new properties. Each value is a new value of the property, a JSDataDescriptor, or a JSAccessorDescriptor. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The method defines the properties with the names specified by KeyValuePair.Key. Please see DefineProperty for the allowed values. Reference semantics of objects is supported. When the same object (which is an independent value) is in different parts of this parameter, the same JavaScript value is used. In particular, you can create objects and properties/element values that form circular references. |  |  | 
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