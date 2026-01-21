---
title: "01-entrystring"
css: "abcpdf-docs.css"
---

|  |  | EntryString Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `string` | null | No | This property represents the path to the file. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property represents the path to the file. It is an required entry and defined as part of the PDF 1.0 specification. This type of file specification always uses the forward slash character for directory separation. Because different platforms use different directory separator characters, it is necessary to translate this string for use on different platforms. If a file name or directory actually contains a forward slash, this needs to be indicated by using a backslash to escape it. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 100. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>