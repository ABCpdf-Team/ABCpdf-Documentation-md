---
title: "apply"
css: "abcpdf-docs.css"
---

|  |  | Apply Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Apply the effect to an image. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Apply(PixMap pixMap) ``` [Visual Basic] ``` Sub Apply(pixMap As PixMap) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| pixMap | The PixMap to which the image should be applied. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Apply the effect to an image specified as a PixMap. Effects normally involve wholesale changes and so it may well be necessary to change the color space and depth in order to apply the effect. If the AutoRestore property is set then the PixMap will be restored to a similar color space after processing and it will be recompressed at an appropriate quality. This default is generally what is required. If the AutoRestore property is not set then the final output may well have different characteristics such as color space and depth. In general the final image will be uncompressed eight bit RGB no matter what type of PixMap was supplied. If you are relying on particular characteristics present in the original PixMap then you should set the AutoRestore property to false and then convert or recolor it after the effect has been applied. Since the final image will be left uncompressed you will likely want to recompress it using an appropriate schema. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: Page GetBitmap Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>