# Flags Property

## Notes

The Font Descriptor Flags entry.

The FontFlags type is a flags type enumeration so the different values can be combined together using bitwise operations. It may take the following values:

The flags detailed here are descriptive. So reading them from an existent font object will provide information on the style. However changing them will not necessarily change it. If the font is referenced then the viewing application will need to find an appropriate system font and it should try to take account of these flags. However if the fonts is embedded then changing the flags will not change the underlying embedded font. Make sure you understand these concepts before you change these values.

How do I manipulate flags enumerations?

To check a flag you can write code of the following form:

[C#] bool isSymbolic = font.Flags.HasFlag(FontObject.FontFlags.Symbolic); [Visual Basic] Dim isSymbolic As Boolean = font.Flags.HasFlag(FontObject.FontFlags.Symbolic)

To set the flag:

[C#] font.Flags |= FontObject.FontFlags.Symbolic; [Visual Basic] font.Flags = font.Flags Or FontObject.FontFlags.Symbolic

To clear the flag:

[C#] font.Flags &= !FontObject.FontFlags.Symbolic; [Visual Basic] font.Flags = font.Flags And Not FontObject.FontFlags.Symbolic

## Example

None.

