---
title: "contentitem"
css: "abcpdf-docs.css"
---

|  |  | ContentItem Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp ContentItemType ``` [Visual Basic]`ContentItemType` | Default | No | Gets or sets the content items to process. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td></tr></tbody></table></td></tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| The ContentItemType enumeration may take the following values: Default – specifies that module-specific default settings should be used. Content – specifies to import only main content. WithMarkup – specifies to import main content and mark-up. This property is currently used only when importing MS Word-supported documents using the MSOffice read module. While the Content setting does allow the import of comments (popup or postit note type structures) they are non-interactive. If this is something you require you may prefer the RichConversion property. |  |  | 
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