---
title: "skiprevisions"
css: "abcpdf-docs.css"
---

|  |  | SkipRevisions Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | 0 | No | Skip back a number of revisions when reading an incrementally saved PDF document. | 

</TD><TD width=60>&nbsp;</TD><TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Skip back a number of revisions when reading an incrementally saved PDF document. PDF documents can be incrementally updated so that changes are appended to the document rather than overwriting the original. This means that it is possible to revert back to a previous version of the document. Setting this value allows you to skip back a specified number of revisions. See the IndirectObject.Revision property and the ObjectSoup.Revisions property for determining the number of revisions a document contains and the content which is associated with each revision. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>