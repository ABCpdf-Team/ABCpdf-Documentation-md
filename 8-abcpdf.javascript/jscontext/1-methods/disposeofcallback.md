---
title: "disposeofcallback"
css: "abcpdf-docs.css"
---

|  |  | DisposeOfCallback Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Disposes of a delegate used to create a JavaScript function. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void DisposeOfCallback(Func func) ``` [Visual Basic]`Sub DisposeOfCallback(func As Func(Of JSCallInfo, Object))` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| func | A delegate used to create a JavaScript function. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Delegates need to be kept alive while the native code may call them. Additionally, a managed API is provided to access the parameters from the native code, so the native code does not call the delegates directly. Therefore, all delegates for which a JavaScript function is created are maintained by the JavaScript context. If your code creates JavaScript functions (including property accessors) for tens of thousands (or more) of distinct delegates (in the sense of reference equality), you may need to dispose of delegates that are no longer callable from JavaScript code. Your code does not need to call this method if it creates only a small number of JavaScript functions using managed delegates. Delegates that are disposed of in this way can later be used to create new JavaScript functions. Do not dispose of delegates that are still callable from JavaScript code. |  |  | 
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