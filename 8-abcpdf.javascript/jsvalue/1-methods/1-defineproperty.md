---
title: "1-defineproperty"
css: "abcpdf-docs.css"
---

|  |  | DefineProperty Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Defines this object's own property. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void DefineProperty(string name, object value) ``` [Visual Basic]`Sub DefineProperty(name As String, value As Object)` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| name | The name of the property. | 
| value | A new value of the property, a JSDataDescriptor, or a JSAccessorDescriptor. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The method defines the property with the specified name. In addition to the independent values (supported by JSContext.ConvertToJS), the value parameter can be a property descriptor. JSDataDescriptor and JSAccessorDescriptor are classes for specifying data descriptor and accessor descriptor, respectively. If in JSAccessorDescriptor, both the delegate property (e.g. Get) and the JavaScript-value property (e.g. JSGet) are non-null/non-Nothing, the delegate property takes precedence for that accessor. Please refer to JavaScript documentation on how to use property descriptors on Object.defineProperty for details. |  |  | 
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