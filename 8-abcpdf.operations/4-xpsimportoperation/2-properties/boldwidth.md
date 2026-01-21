---
title: "boldwidth"
css: "abcpdf-docs.css"
---

|  |  | BoldWidth Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp double ``` [Visual Basic]`Double` | 1.0 | No | The percentage of boldness to apply when creating a synthetic bold style. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property specifies the percentage of boldness to apply when creating a synthetic bold style. XPS documents can contain text in simulated bold. Simulated bold is used where a font does not have a bold variant and a synthetic approximation is required. However this is a feature which is specific to XPS and which does not have an analog in PDF. So this means that during the import process ABCpdf has to create an appropriate synthetic bold substitute. The XPS specification says that this should be done using an outline which is 1% of the size of the font. However this level of emboldenment can look somewhat lighter than one might expect. By increasing the value of this property you can make such fonts look more bold. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14></TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>