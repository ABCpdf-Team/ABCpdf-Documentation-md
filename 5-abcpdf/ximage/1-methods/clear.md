---
title: "clear"
css: "abcpdf-docs.css"
---

|  |  | Clear Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Clears the image. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Clear() void Clear(out XReadOptions outOptions, out Stream outStream) ``` [Visual Basic] ``` Sub Clear() Sub Clear( ByRef outOption As XReadOptions, ByRef outStream As Stream) ``` |  |  | 
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
      
| Use this method to release resources and return the image to a just-created state. The overload without parameters disposes of the XReadOptions and of the Stream. The overload with output parameters returns the XReadOptions and the Stream. The returned objects have not been disposed of. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
|  |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>