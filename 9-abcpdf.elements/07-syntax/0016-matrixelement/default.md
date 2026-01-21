---
title: "default"
css: "abcpdf-docs.css"
---

# MatrixElement Class

This class represents a tranformation matrix.

Transformation matrices can be used to produce affine transforms such as translations, scales, rotations and skews.

A transformation matrix consists of an array of six values.

Coordinates are expressed as a three element matrix:.

[x, y, 1].

The transformation matrix is expressed as a three by three matrix:.

[a, b, 0].

[c, d, 0].

[e, f, 1].

So to apply a matrix to a point or set of points one simply multiplies the point matrix by the transformation matrix.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 119.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=127)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.MatrixElement ```

## Method Description MatrixElement Create a new MatrixElement. inherited methods... &nbsp;

## Property Description Elements The six elements in this list represent the following elements of the three by three transformation matrix:. inherited properties...