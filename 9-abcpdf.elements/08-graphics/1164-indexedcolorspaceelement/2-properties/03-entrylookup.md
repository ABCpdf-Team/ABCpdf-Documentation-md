# EntryLookup Property

## Notes

This property represents the lookup table for the palette.

The lookup may be represented as a StreamElement or (in PDF 1.2) a byte string.

The table shall contain a number of colors one higher than the EntryHiVal.

Each color shall contain a number of byes equal to the number of components in the EntryBaseColorSpace.

Each byte represents an intensity of color from 0 to 255 - 0% to 100% respectively.

For definitive details see:.

The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 156.
