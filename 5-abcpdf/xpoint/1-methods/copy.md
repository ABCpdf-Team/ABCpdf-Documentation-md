---
title: "copy"
css: "abcpdf-docs.css"
---

|  |  | Copy Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Copies a series of X and Y coordinates between arrays of doubles and arrays of XPoints |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void Copy(XPoint[] source, double[] destination, int length) void Copy(XPoint[] source, int sourceIndex, double[] destination, int destinationIndex, int length) void Copy(double[] source, XPoint[] destination, int length) void Copy(double[] source, int sourceIndex, XPoint[] destination, int destinationIndex, int length) ``` [Visual Basic] ``` Sub Copy(source() As XPoint, destination() As Double, length As Integer) Sub Copy(source() As XPoint, sourceIndex As Integer, destination() As Double, destinationIndex As Integer, length As Integer) Sub Copy(source() As Double, destination() As XPoint, length As Integer) Sub Copy(source() As Double, sourceIndex As Integer, destination() As XPoint, destinationIndex As Integer, length As Integer) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| source | An array of points to be copied from. | 
| destination | An array of points to be copied to. | 
| length | The number of points that should be copied. | 
| sourceIndex | The index in the source array at which copying begins. | 
| destinationIndex | The index in the destination array at which copying begins. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Copies a series of X and Y coordinates between arrays of doubles and arrays of XPoints. The array of doubles is represented as a series of pairs of X and Y coordinates. So the double array should always be twice the length of the XPoint array. Indexes into the arrays are specfied in terms of items in the array. This means that indexes into a double array will be twice as large as those into an XPoint array. Lengths are always specified in terms of numbers of points rather than number of items in the array. In the case of copying to an array of XPoints, each XPoint in the destination array will be newly created from the source array values overwriting any XPoint which may already be at that location in the array. |  |  | 
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