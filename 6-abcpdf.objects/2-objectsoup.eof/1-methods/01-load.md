---
title: "01-load"
css: "abcpdf-docs.css"
---

|  |  | Load Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Loads the file trailer data. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Load(ObjectSoup soup) ``` [Visual Basic] ``` Function Load(soup As ObjectSoup) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| soup | The ObjectSoup of a Doc object. The Doc must have been loaded using Doc.Read. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Loads the file trailer data. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code tests to see if any of the revisions in a document are hybrid. [C#] ```csharp bool isHybrid = false; using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/sample.pdf")); using (var eof = new ObjectSoup.Eof()) { eof.Load(doc.ObjectSoup); var xref = eof.XRef; while (xref != null) { if (xref.Type == ObjectSoup.XRefType.Hybrid) { isHybrid = true; break; } xref = xref.Prev; } } // do something with isHybrid ``` [Visual Basic] ```vbnet Dim isHybrid As Boolean = False Using doc = New Doc() doc.Read(Server.MapPath("../mypics/sample.pdf")) Using eof = New ObjectSoup.Eof() eof.Load(doc.ObjectSoup) Dim xref = eof.XRef While xref <> Nothing If xref.Type = ObjectSoup.XRefType.Hybrid Then isHybrid = True Exit While End If xref = xref.Prev End While ' do something with isHybrid End Using End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>