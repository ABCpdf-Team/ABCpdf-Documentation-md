---
title: "substitutions"
css: "abcpdf-docs.css"
---

|  |  | Substitutions Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp IDictionary ``` [Visual Basic] `IDictionary` | n/a | No | A set of character to string substitutions used for translating typographic characters like ligatures into more normal text. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| A set of character to string substitutions used for translating typographic characters like ligatures into more normal text. PDF text often includes typographic characters that are uncommon in normal text. For example these may include ligatures such as 'ff' or 'fl'. They may include different types of dash such as n-dash and m-dash. They may include curly/smart single and double quote characters. For the purposes of text extraction and searching it is generally desirable to replace these characters with their more common equivalents. The default settings for this operation include the substitutions of the types of characters detailed above. The default settings are liable to change so if it is important that your settings remain constant between different versions of ABCpdf you should assign your own values. |  |  | 
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