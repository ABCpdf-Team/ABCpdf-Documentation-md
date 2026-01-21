# XPoint Class

Represents a point in two-dimensional space. When first created the object defaults to the origin "0 0" which is at the bottom left of the space.

ABCpdf uses the standard Adobe PDF coordinate space. The origin of this space is at the bottom left of the document. Distances are measured up and right in points. Points are a traditional measure for print work and there are 72 points in an inch. For further details see the [Coordinates](../../2-getting_started/3-coordinates.md) section of the documentation.

``` System.Object WebSupergoo.ABCpdf13.XPoint Implements: IDisposable, IEquatable, IComparable ```

## Method Description XPoint XPoint Constructor. Copy Copies a series of X and Y coordinates between arrays of doubles and arrays of XPoints. Equals Test whether the two points are effectvely the same. GetHashCode A hash code for the XPoint. SetPoint Sets the point. ToString Returns a string representation of the object. &nbsp;

## Property Description Point The System.Drawing.Point. String The point as a string. X The horizontal coordinate. Y The vertical coordinate.