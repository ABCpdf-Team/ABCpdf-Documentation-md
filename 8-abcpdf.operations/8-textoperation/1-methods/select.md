---
title: "select"
css: "abcpdf-docs.css"
---

|  |  | Select Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Select a range of text in the document. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IListTextFragment> Select(int startIndex, int length) ``` [Visual Basic] `Function Select(startIndex As Integer, length As Integer) As IListTextFragment>` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| startIndex | The start index for the selection as related to the string returned by the GetText method. | 
| length | The length for the selection as related to the string returned by the GetText method. | 
| Return | Returns a list of find matches encompassing the selected text. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Select a range of text in the document. If GetText has not been called previously then an exception will be raised. This function is purposely designed to be similar to the String.Substring function. The concept is that you can use the text provided via the GetText method to identify pieces of text you are interested in. Then using the offset and length of the pieces you can select the actual text in the document. The selection specifies the precise set of text fragments in the document. Each fragment has an area, some text and relates back to a text drawing operation within the content stream of the page. Applying the Group function to these fragments can group connected fragments into connected parts. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Group function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>