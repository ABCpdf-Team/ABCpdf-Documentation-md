# Pin Property

## Notes

Allows you change the pinned corner of the rectangle.

The Corner enumeration may take the following values:

Some operations require that the rectangle is pinned to a location. For example if you want to change the width of a rectangle you can do this either by shifting the left side or the right side. If the pin property is set to the bottom or top left then the left side of the rectangle will be kept fixed and the right side shifted. Conversely if the pin property is set to the bottom or top right then the right side of the rectangle will be kept fixed and the left side shifted.

Why is my Pin a number?

In older versions of ABCpdf the Pin property was a number. To assign a Corner to the Pin property you needed to cast the value. So you might find code of this form.

[C#] theRect.Pin = (int)XRect.Corner.TopRight;

In Version 8 the Pin property has been changed to a true enumeration. This means you can assign the Corner directly.

[C#] theRect.Pin = XRect.Corner.TopRight;

If your code is bound to integers rather than enumerations then it is safe to cast the number to a Corner.

[C#] theRect.Pin = (XRect.Corner)myIntegerValue;

## Example

Also see example code in: ABCpdf eForm Placeholder Example, Doc TopDown Property, XRendering DrawAnnotations Property, Page GetBitmap Function, PixMap SetAlpha Function, PixMap ToGrayscale Function.

