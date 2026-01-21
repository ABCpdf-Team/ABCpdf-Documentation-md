---
title: "textwidth"
css: "abcpdf-docs.css"
---

|  |  | TextWidth Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Calculate the width of a string of text. |  |  | 

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| **[C#]** ```csharp int TextWidth(string text) ``` [Visual Basic]`Function TextWidth(text As String) As Integer` |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| Name | Description | 
| --- | --- |
| text | The text | 
| return | The width of the text in 1000ths. | 

</TD><TD width=60>&nbsp;</TD><TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| This function caculates the width for a given text string.The value returned is measured in thousandths of a unit. So to calculate the physical size on the page multiply the returned value by the font size and divide by one thousand. |  |  | 
| --- | --- | --- |

</TD></TR> 
<TR> <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD><TD width=14>&nbsp;</TD><TD vAlign=top> 

| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>