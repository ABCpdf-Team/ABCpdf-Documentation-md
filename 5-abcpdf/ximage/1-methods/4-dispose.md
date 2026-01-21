---
title: "4-dispose"
css: "abcpdf-docs.css"
---

|  |  | Dispose Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Dispose of the object. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Dispose() void Dispose(out XReadOptions outOptions, out Stream outStream) protected void Dispose(bool disposing) ``` [Visual Basic] ``` Sub Dispose() Sub Dispose( ByRef outOption As XReadOptions, ByRef outStream As Stream) Protected Sub Dispose(disposing As Boolean) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| outOptions | The XReadOptions used to create the object. | 
| outStream | The Stream used to create the object if NeedsStream is true. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| You can call this function to explicitly dispose of an object and reduce the garbage collection overhead. The overload without parameters disposes of the XReadOptions and of the Stream. The overload with output parameters returns the XReadOptions and the Stream. The returned objects have not been disposed of. This method follows the standard design pattern for objects implementing the IDisposable interface. The protected Dispose method can be overridden for sub-classes wishing to dispose of additional objects. Do not attempt to use an object after calling Dispose. |  |  | 
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