---
title: "05-reportentryversion"
css: "abcpdf-docs.css"
---

|  |  | ReportEntryVersion Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Called to report the entry version. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ReportEntryVersion(string entry, PDFVersion version) ``` [Visual Basic] ``` Overridable Function ReportEntryVersion(entry As string, version As PDFVersion) As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| entry | The entry name. | 
| version | The PDF version. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Called to report the entry version. Dictionaries are validated item by item for each of the key value pairs. Each key is associated with a particular PDF Version in which it was introduced. This function is called for each entry, with a number indicating the minimum version required. The PDFVersion type is a flags type enumeration so different values can be combined together using bitwise operations. It may take the following values: None - No version information available. PDF10 - Introduced in PDF 1.0. PDF11 - Introduced in PDF 1.1. PDF12 - Introduced in PDF 1.2. PDF13 - Introduced in PDF 1.3. PDF14 - Introduced in PDF 1.4. PDF15 - Introduced in PDF 1.5. PDF16 - Introduced in PDF 1.6. PDF17 - Introduced in PDF 1.7. PDF17Obsolescent - Obsolescent in PDF 1.7. AdobeUndocumented - Adobe undocumented extension. PDF17Extension3 - Introduced in PDF 1.7 Adobe Extension Level 3. PDF17Extension5 - Introduced in PDF 1.7 Adobe Extension Level 5. PDF20 - Introduced in PDF 2.0. PDF20Deprecated - Deprecated in PDF 2.0. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>