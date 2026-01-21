---
title: "errorhandling"
css: "abcpdf-docs.css"
---

|  |  | ErrorHandling Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp ErrorHandlingType ``` [Visual Basic]`ErrorHandlingType` | OutputUntilError | No | The error handling behavior. | 

</TD><TD width=60>&nbsp;</TD><TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| The ErrorHandlingType enumeration may take the following values: OutputUntilErrorNoOutputOnErrorThe OutputUntilError directs ABCpdf to process the current file as far as possible even if it encounters an error. This can be useful for dealing with common forms of corruption. For example EPS files sometimes get truncated. As long as the truncation is small the output will be the same as the complete file despite the fact that from technical point of view these files are invalid.However one cannot know exactly how small a truncation is. It might be that one needs to be absolutely sure that a file is valid; that it is better to throw an exception rather than risk an incomplete image. This behavior is achieved using NoOutputOnError. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>