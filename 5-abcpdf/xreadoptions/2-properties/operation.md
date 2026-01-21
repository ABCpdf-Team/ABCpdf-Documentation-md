---
title: "operation"
css: "abcpdf-docs.css"
---

|  |  | Operation Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Operation ``` [Visual Basic]`Operation` | null | No | Gets or sets the Operation to use. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property is used by modules for which a suitable derived class of Operation exists. If it is null, those modules create a temporary Operation with default behaviours. ReadModule | Operation | Description | 
| --- | --- | --- |
| SwfVector | SwfImportOperation | If this property is null, the temporary SwfImportOperation has its Timeout set to Timeout and sets ProcessingObjectEventArgs.Info.FrameNumber to Frame once. | 
| Xps | XpsImportOperation | If this property is null, the temporary XpsImportOperation compresses the GraphicLayer's of the pages. | 
| XpsAny | XpsImportOperation | If this property is null, the temporary XpsImportOperation compresses the GraphicLayer's of the pages. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>