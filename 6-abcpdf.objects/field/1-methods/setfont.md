---
title: "setfont"
css: "abcpdf-docs.css"
---

|  |  | SetFont Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sets the font and font size to be used for text |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp vitual void SetFont(FontObject font, double size) ``` [Visual Basic] ``` Sub SetFont(font As FontObject, size As Double) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| font | The font to be assigned to the field. | 
| size | The font size to be assigned to the field. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Sets the font and font size to be used for text. This function works by changing the DefaultAppearance for the field using the specified FontObject and size. Properties such ase the TextFont and TextSize get the effective value which may be inherited. Calling this funtion sets the value on this item itself which will override any inherited value. Passing a font value of null will remove both the font and size from the item itself though a value may be still be present if it is inherited from a parent field or from document defaults. A zero size font indicates that the font should scale so that it fits the size of the field. Negative font heights appear the same as positive ones but are best avoided as they are likely to cause confusion. The appearance of the field is not updated until you change the Value or call UpdateAppearance. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>