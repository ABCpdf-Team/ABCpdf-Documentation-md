---
title: "focus"
css: "abcpdf-docs.css"
---

|  |  | Focus Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Prepare document for drawing at the fragment location. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Focus() ``` [Visual Basic] ``` Sub Focus() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| none |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to focus on the fragment. This prepares the document for drawing at the fragment location. After calling this function you can add content overlaying the fragment. For example you might call Doc.FillRect to overlay it. Text is drawn at a height of one point, using a transformation matrix to scale it up. So, in general, after calling this method, the Doc.Rect Height will be 1.0. The Doc.Page, Doc.Rect and Doc.Transform may all be changed as a result of calling this method. |  |  | 
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