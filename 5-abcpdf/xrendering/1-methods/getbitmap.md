---
title: "getbitmap"
css: "abcpdf-docs.css"
---

|  |  | GetBitmap Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Renders the current area of the current page to a Bitmap. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp System.Drawing.Bitmap GetBitmap() ``` [Visual Basic]`Function GetBitmap() As System.Drawing.Bitmap` `may throw Exception()` |  |  | 
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
      
| Use this method to render the PDF to a System.Drawing.Bitmap. The output is a render of the current Doc.Rect of the current Doc.Page. Any page rotation specified in the PDF page is applied so that the output render is the correct orientation. This may mean that the output width and height are transposed copies of the width and height as specified in the Doc.Rect. You can then use this Bitmap for drawing to screen or for manipulation using System.Drawing routines. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the AntiAliasPolygons property. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>