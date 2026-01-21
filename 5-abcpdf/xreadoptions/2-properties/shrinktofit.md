---
title: "shrinktofit"
css: "abcpdf-docs.css"
---

|  |  | ShrinkToFit Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic]`Boolean` | true | No | Whether to try and determine the document size based on the size of the content. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Some formats such as SVG contain a viewport wrapper and then a viewbox containing content. The size of the viewport can be specified - much the same as specifying the size of paper on which something should be printed. However similarly you can specify the size of the content without specifying the size of the viewport - much the same as saying that the drawing is a certain size without dictating the size of the paper. This is quite a common situation for web output where you want the content to be drawn in a browser window and you do not know what size the user will select for that window. If this property is set to true, the page size will be set to be the same as the content viewbox. This effectively shrinks the page to fit the content avoiding excessive white space or clipping. If this property is set to false, the page size is taken from the DefaultRect property and the content is centered on this page. The viewbox size is inserted as the page ArtBox for possible use at a later stage. |  |  | 
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