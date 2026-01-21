---
title: "fontsubstitution"
css: "abcpdf-docs.css"
---

|  |  | FontSubstitution Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp FontSubstitutionType ``` [Visual Basic]`FontSubstitutionType` | FontSubstitutionType.Automatic | No | The font substitution type. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property specifies when fonts are substituted in export operations. Only the DOCX and HTML exporters currently support this property. It is ignored by other exporters, for example, the XPS exporter. The FontSubstitutionType enumeration may take the following values: Automatic - selects a sensible default value based on the exporter. Always - always substitute fonts with those installed on the machine. Missing - only substitute fonts which are missing or could not be converted to open type. |  |  | 
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