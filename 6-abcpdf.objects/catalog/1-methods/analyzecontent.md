---
title: "analyzecontent"
css: "abcpdf-docs.css"
---

|  |  | AnalyzeContent Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Perform whole document analysis of page contents. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp void AnalyzeContent() ``` [Visual Basic] `Function AnalyzeContent()` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| none |  | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This function scans the document and performs analysis of the contents. Scanning the document content involves decompressing and parsing all the content in the document. As such it can be an expensive and time consuming process for large or complex documents. For this reason the analysis is cached the first time this function is called. If you later change the content it is your responsibility to call this function to ensure that the analysis is updated. Whole document analysis enables certain other optimizations such as Font.Subset. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>