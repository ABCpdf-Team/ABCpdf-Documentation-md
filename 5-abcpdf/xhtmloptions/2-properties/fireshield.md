---
title: "fireshield"
css: "abcpdf-docs.css"
---

|  |  | FireShield Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XHtmlFireShield ``` [Visual Basic]`XHtmlFireShield` | null | No | The FireShield™ security settings to be applied to the ABCChrome engine. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This proprerty determines the security settings which should be applied to HTML conversion using the ABCChrome engine. The problem with most sandboxes is they are not sufficiently dynamic. You may want to allow access to a specific file or set of files for one request, while prohibiting acces to those same files for another. FireSheld allows you to configure per-request permissions using an easy to understand rule based system. It reports permission issues in an obvious way so that if you need to troubleshoot access problems, it is trivial to work out what is going wrong. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code snippet illustrates how one might add a rule to allow access to an audio driver or similar. [C#] ```csharp using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.Chrome123; doc.HtmlOptions.FireShield.Rules.Add(new XHtmlFireShield.PathRule(@"C:\Windows\*.drv", XHtmlFireShield.PathRule.AccessType.Allow)); int id = doc.AddImageUrl("https://www.google.com/"); // ... ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.Chrome123 doc.HtmlOptions.FireShield.Rules.Add(New XHtmlFireShield.PathRule("C:\Windows\*.drv", XHtmlFireShield.PathRule.AccessType.Allow)) ' ... Dim id As Integer = doc.AddImageUrl("https://www.google.com/") End Using ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>