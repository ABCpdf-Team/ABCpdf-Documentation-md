---
title: "frame"
css: "abcpdf-docs.css"
---

|  |  | Frame Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp long ``` [Visual Basic]`Long` | 0 | No | The frame to be read from a multiple frame image such as a movie. | 

</TD><TD width=60>&nbsp;</TD><TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| This property is used by read modules that support frames or sub-documents. Frames are numbered from one upwards. The default of zero indicates that a default frame or frame set should be used. The SwfVector module uses this property when the Operation is null. When this occurs a temporary SwfImportOperation is created and the ProcessingObjectEventArgs.Info.FrameNumber is set to the value of this property. The default behavior is to read frame one. The MSOffice module uses this property to allow you to read individual worksheets from within an Excel spreadsheet. The default behavior is to read all the worksheets in order rather than simply select one of them. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>