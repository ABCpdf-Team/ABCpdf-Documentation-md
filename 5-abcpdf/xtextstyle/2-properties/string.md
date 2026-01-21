---
title: "string"
css: "abcpdf-docs.css"
---

|  |  | String Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic]`String` | Variable | No | The text style as a string. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| A string representation of the text style. This covers all the properties of this class and can be sued for a save and restore stack. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following code. [C#] ```csharp var ts = new XTextStyle(); ts.String = "24.5 10 0 0 0 0 0"; Response.Write($"Size = {ts.Size}"); Response.Write($"Indent = {ts.Indent}"); ``` [Visual Basic] ```vbnet Dim ts As New XTextStyle() ts.String = "24.5 10 0 0 0 0 0" Response.Write($"Size = {ts.Size}") Response.Write($"Indent = {ts.Indent}") ``` Produces the following output. Size = 24.5Indent = 10 |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>