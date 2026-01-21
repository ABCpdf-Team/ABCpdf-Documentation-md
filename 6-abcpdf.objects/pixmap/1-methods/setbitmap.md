---
title: "setbitmap"
css: "abcpdf-docs.css"
---

|  |  | SetBitmap Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Set the content of the object as a Bitmap |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void SetBitmap(System.Drawing.Bitmap bitmap, bool transparent) ``` [Visual Basic] ``` Sub SetBitmap(bitmap As System.Drawing.Bitmap, transparent As Boolean) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| bitmap | The Bitmap containing the image. | 
| transparent | Whether any transparency information should be preserved. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Set the content of the object as a System.Drawing.Bitmap. If transparency is required, the PixMap must be contained within an ObjectSoup. After the Bitmap has been set, the PixMap will be uncompressed. You may wish to compress it using a call like CompressJpeg or CompressFlate. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the Doc.AddXObject method..Also see example code in: Doc AddXObject Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>