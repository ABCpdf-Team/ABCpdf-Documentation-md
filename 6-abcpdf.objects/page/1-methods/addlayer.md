---
title: "addlayer"
css: "abcpdf-docs.css"
---

|  |  | AddLayer Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add a content layer to the page |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void AddLayer(string text) void AddLayer(byte[] data) void AddLayer(StreamObject stream) void AddLayer(string text, int index) void AddLayer(byte[] data, int index) void AddLayer(StreamObject stream, int index) ``` [Visual Basic] ``` Function AddLayer(text As String) As Integer Function AddLayer(data As Byte()) As Integer Function AddLayer(stream As StreamObject) As Integer Function AddLayer(text As String, index As Integer) As Integer Function AddLayer(data As Byte(), index As Integer) As Integer Function AddLayer(stream As StreamObject, index As Integer) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| text | The ASCII text to be added - typically a set of PDF drawing operators. | 
| data | The data to be added - typically an ASCII representation of a set of PDF drawing operators. | 
| stream | The stream that should be added as a new layer on page. | 
| index | The index at which the layer should be added. If the index is greater than or equal to the number of layers then the new layer will be added at the top. Default Int.Max. | 
| return | The Object ID of the newly added StreamObject. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add a content layer to the page. By default the layer will go at the top or front of the page. By supplying an index parameter you can position your new layer behind other layers that already exist. Layers draw in sequence when displayed which means that later layers may draw over the top of earlier layers. Any StreamObject that is supplied should contain PDF drawing operations. The data and text overloads are convenience functions for common operations. You will need to ensure that any resources that are referenced in this content stream have been added to the resources of the page using a method such as AddResource. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Also see example code in: Page MakeFormXObject Function, OpAtom Find Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>