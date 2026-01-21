---
title: "gettaguntransformedrects"
css: "abcpdf-docs.css"
---

|  |  | GetTagUntransformedRects Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets an array of the locations of tagged visible items before Doc.Transform is applied. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp XRect[] GetTagUntransformedRects(int id) ``` [Visual Basic]`Function GetTagUntransformedRects(id As Integer) As XRect()` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| id | The Object ID of the object. | 
| return | The location (before Doc.Transform is applied) of tagged visible HTML objects. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to retrieve the locations of tagged visible items. The locations are to be used with the value of Doc.Transform the same as when the ID is obtained. To use this method you need to enable the tagging functionality. See the AddTags property for details. This function takes an ID obtained from a call to Doc.AddImageUrl, Doc.AddImageHtml or Doc.AddImageToChain and returns the locations of any items which are visible on the PDF page as a result of that call. The locations match up directly on a one-to-one basis with the IDs returned by the GetTagIDs function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| See the GetTagRects method. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>