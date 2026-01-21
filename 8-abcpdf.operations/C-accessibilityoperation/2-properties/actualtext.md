---
title: "actualtext"
css: "abcpdf-docs.css"
---

|  |  | ActualText Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to embed the actual text of text elements. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Whether to embed the actual text of text elements. It is often useful to embed the actual text of PDF content in the tag structure because this makes it easy to extract. Extracting text from the content stream is extremely difficult in comparison. There is a standard tag - ActualText - provided for this very purpose. Unfortunately there are problems in some releases of Acrobat that mean that the presence of this tag can make it difficult to select and extract text. As such you may wish to set this property to false to avoid this type of structure. |  |  | 
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