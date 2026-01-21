---
title: "embeddedfile"
css: "abcpdf-docs.css"
---

|  |  | EmbeddedFile Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| EmbeddedFile Constructor |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp EmbeddedFile(ObjectSoup soup) EmbeddedFile(ObjectSoup soup, string path) EmbeddedFile(ObjectSoup soup, byte[] data) ``` [Visual Basic] ``` Sub New(soup As ObjectSoup) Sub New(soup As ObjectSoup, path As String) Sub New(soup As ObjectSoup, data() As Byte) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created EmbeddedFile. | 
| path | A path to a file containing data which should be placed in the EmbeddedFile. | 
| data | An array of bytes which should be placed in the EmbeddedFile. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create an EmbeddedFile. This constructor which takes a path to a file will embed and compress the file data using using the CompressFlate function. It will also insert appropriate metadata using the UpdateMetadata function. The constructor which takes an array of data will similarly embed and compress the data. However since there is no file path metadata will not be assigned. |  |  | 
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