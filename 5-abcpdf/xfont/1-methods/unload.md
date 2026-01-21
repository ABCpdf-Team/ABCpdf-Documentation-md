---
title: "unload"
css: "abcpdf-docs.css"
---

|  |  | Unload Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Unloads a font so that it is no longer available. |  |  | 

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| **[C#]** ```csharp void Unload() ``` [Visual Basic] `Sub Unload()` |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Name | Description | 
| --- | --- |
| none |  | 

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Unloads a font so that it is no longer available. It is important that you ensure that the fonts is not being used by ABCpdf at the point that it is unloaded. This means you need to consider if other threads might be constructing PDF documents that are making use of the font. Unloading a font which is in use may result in unpredictable behavior or output. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>