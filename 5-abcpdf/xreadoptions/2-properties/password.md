---
title: "password"
css: "abcpdf-docs.css"
---

|  |  | Password Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic]`String` | null | No | Gets or sets the password needed to read the source. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td></tr></tbody></table></td></tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| Specify with this property the password for accessing the source, for example, when reading a PDF document. It is used for importing MS Word or MS Excel documents when using Microsoft Office via the XpsAny and MSOffice ReadModule. Note that for other Office applications, eg. MS PowerPoint, ABCpdf cannot import password protected documents. Currently, certain features such as form fields conversion may be disabled if the document is password protected, even if the correct password is supplied. |  |  | 
| --- | --- | --- |

</td></tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| None. |  |  | 
| --- | --- | --- |

</td></tr></tbody></table>