# DefaultAppearance Property

## Notes

The default appearance (DA) used for the text.

The ArrayAtom is a sequence of PDF parameters and operators which makes up a complete drawing sequence.

This property controls the base set of drawing instructions used for controlling the appearance of variable text in a field. Getting this property gets the effective value which may be inherited. Setting this property sets the value on this item itself.

Similarly setting this property to null will remove the property on the item itself but the value may continue to be inherited. The appearance of the field is not updated until you change the Value or call UpdateAppearance.

## Example

None.

