# XColor Class

This object represents a color. Colors may be expressed in RGB, CMYK, Grayscale or generic unspecified color components.

When first created, the color defaults to RGB black - "0 0 0".

``` System.Object WebSupergoo.ABCpdf13.XColor Implements: IDisposable, IEquatable, IComparable ```

## Method Description S&raquo;&nbsp; FromGray Create an XColor from a grayscale value. S&raquo;&nbsp; FromRgb Create an XColor from a set of RGB component values. S&raquo;&nbsp; FromCmyk Create an XColor given a set of CMYK component values. S&raquo;&nbsp; FromComponents Create an XColor from a set of PDF components in the generic ColorSpace color space. S&raquo;&nbsp; &nbsp;FromArrayAtom Create an XColor from an ArrayAtom of NumAtoms containing PDF color values. S&raquo;&nbsp; &nbsp;FromOperator Create an XColor given a PDF color operator and a set of Atoms containing the arguments for that operator. SetColor Sets the color. SetGray Set the color to a grayscale value. SetRgb Set the color to an RGB value. Equals Test whether the two colors are effectively the same. GetHashCode A hash code for the XColor. SetCmyk Set the color to an CMYK value. SetComponents Set the color to a set of ColorSpace PDF components. SetRandom Set the color to a random opaque value in the current color space. ToArrayAtom An ArrayAtom representation of the components of the color. ToString Returns a string representation of the object. &nbsp;

## Property Description Alpha The alpha opacity. Black The black component. Blue The blue component. Color The System.Drawing.Color. ColorSpace The native color space for the color. Components The components of the color in native PDF format. Cyan The cyan component. Gray The gray component. Green The green component. Magenta The magenta component. Name Any name that may be associated with this color. Red The red component. String The color as a string. Yellow The yellow component.