---
title: "gettext"
css: "abcpdf-docs.css"
---

|  |  | GetText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Extract content from the current page in a specified format. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string GetText(string type) string GetText(Page.TextType type, bool includeAnnotations) ``` [Visual Basic] ``` Function GetText(type As String) As String Function GetText(type As Page.TextType, includeAnnotations As Boolean) As String ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| type | The format in which to return the content. | 
| includeAnnotations | Whether to include field and annotation text. | 
| return | The returned content. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This function allows you to extract the content from a page. This is a convenience function for easy access to the content of the current page. For full details of how text extraction works see the Page.GetText function. The following formats are supported - "Text", "SVG", "SVG+", "SVG+2" and "RawText". These types can be specified as strings for backwards compatibility with older code. However in newer code you should prefer the function overload that takes a Page.TextType enumeration. Text is in layout order which may not be the same as reading order. ABCpdf will make sensible assumptions on how items of text should be combined but some situations are ambiguous. The current release of ABCpdf is much more sophisticated than previous ones when it comes to extracting text. However if you are relying on the ABCpdf 8 simplified model you can use the "RawText" format for backwards compatibility. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
|  |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>