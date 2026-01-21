---
title: "stamp"
css: "abcpdf-docs.css"
---

|  |  | Stamp Method |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Stamp all fields into the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Stamp() ``` [Visual Basic]`Sub Stamp()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| none |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to permanently stamp all fields into the document. When this method is called all field appearances are stamped permanently into the document and the fields are deleted. Each field becomes a new layer on the page (see Doc.LayerCount) so you may wish to call Doc.Flatten on any affected pages. You can use the Field.Stamp method to stamp individual fields into the document. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: ABCpdf eForm Stamp Example. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>