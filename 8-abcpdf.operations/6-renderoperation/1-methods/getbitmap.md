---
title: "getbitmap"
css: "abcpdf-docs.css"
---

|  |  | GetBitmap Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Renders a page into a bitmap. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp System.Drawing.Bitmap GetBitmap() ``` [Visual Basic] ``` Function GetData(name As String) As Byte() ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | The Bitmap containing the image. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Renders a page into a Bitmap. The page and rendering options which will be used are those which were current at the time the RenderOperation was created. This method is similar in functionality to XRendering.GetBitmap but allows safe muti-threaded use. For details see the Save method. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Nne. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>