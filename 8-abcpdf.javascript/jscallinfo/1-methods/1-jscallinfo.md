---
title: "1-jscallinfo"
css: "abcpdf-docs.css"
---

|  |  | JSCallInfo Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Creates a new JavaScript call information object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp JSCallInfo(JSContext context, JSValue callee, bool isConstructCall, IList args) ``` [Visual Basic]`Sub New(context As JSContext, callee As JSValue, isConstructCall As Boolean, args As IList(Of JSValue))` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| context | The JavaScript context. This must be non-null/non-Nothing. | 
| callee | The callee. | 
| isConstructCall | Indicates whether the call is a 'new' call. | 
| args | The arguments to the call. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The constructor creates a new JavaScript call information object. |  |  | 
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