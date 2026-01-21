---
title: "gettagids"
css: "abcpdf-docs.css"
---

|  |  | GetTagIDs Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Gets an array of the HTML IDs of tagged visible items. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp string[] GetTagIDs(int id) ``` [Visual Basic]`Function GetTagIDs(id As Integer) As String()` |  |  | 
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
| return | The IDs of tagged visible HTML objects. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to retrieve the HTML IDs of tagged visible items. To use this method you need to enable the tagging functionality. See the AddTags property for details. This function takes an ID obtained from a call to Doc.AddImageUrl, Doc.AddImageHtml or Doc.AddImageToChain and returns the IDs of any items which are visible on the PDF page as a result of that call. For example the ID associated with the following paragraph is "p1". ```html Gallia est omnis divisa in partes tres. ``` The IDs may be repeated if the objects are split over more than one area. The IDs match up directly on a one-to-one basis with the XRects returned by the GetTagRects or the GetTagUntransformedRects function. |  |  | 
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