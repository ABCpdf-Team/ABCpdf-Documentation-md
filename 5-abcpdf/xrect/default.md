---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | XRect Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Represents a rectangular area in two-dimensional space. When first created the object defaults to an empty rectangle "0 0 0 0". ABCpdf uses the standard Adobe PDF coordinate space. The origin of this space is at the bottom left of the document. Distances are measured up and right in points. Points are a traditional measure for print work and there are 72 points in an inch. For further details see the Coordinates section of the documentation. You can change the coordinate system used by the Doc.Rect and the Doc.MediaBox using the Doc.Units and Doc.TopDown properties. ``` System.Object WebSupergoo.ABCpdf13.XRect Implements: IDisposable, IEquatable, IComparable ``` |  |  | 

</TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Method | Description | 
| --- | --- |
| S» FromLbwh | Creates an XRect from a bottom left corner, a width and a height. | 
| S» FromLtwh | Creates an XRect from a top left corner, a width and a height. | 
| S» FromSides | Creates an XRect from the coordinates of two diagonally opposite corners. | 
| S» FromPoints | Create the smallest XRect that encloses all the points supplied. | 
| S» FromAtom | Create an XRect from a standard PDF Rectangle ArrayAtom. | 
| S» FromNums | Create an XRect from an array or list of four numbers. | 
| XRect | XRect Constructor. | 
| Contains | Determine if this rectangle contains a specified point or rectangle. | 
| FitIn | Fits the rectangle as content inside another rectangle. | 
| GetCorners | Get the four corners of the rectangle. | 
| Inset | Insets the edges of the rectangle. | 
| Intersect | Intersects this rectangle with another rectangle. | 
| IntersectsWith | Determine if this rectangle intersects with another. | 
| Magnify | Magnifies the rectangle. | 
| Move | Translate the rectangle. | 
| Position | Position the bottom left of the rectangle. | 
| Resize | Resizes the rectangle. | 
| Union | Union this rectangle with another rectangle. | 
| SetRect | Sets the location and size of the rectangle. | 
| SetSides | Sets the sides of the rectangle. | 
| ToString | Returns a string representation of the object. | 
| Equals | Test whether the two rectangles are effectively the same. | 
| GetHashCode | A hash code for the XRect. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD vAlign=top>&nbsp; </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Property | Description | 
| --- | --- |
| Bottom | The bottom coordinate. | 
| Height | The height of the rectangle. | 
| Left | The left coordinate. | 
| Pin | The corner of the rectangle to pin. | 
| Rectangle | The System.Drawing.Rectangle. | 
| Right | The right coordinate. | 
| String | The rect as a string. | 
| Top | The top coordinate. | 
| Width | The width of the rectangle. | 
| HasArea | Whether the rectangle has area. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR>
        <TR>
          <TD>&nbsp;</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>