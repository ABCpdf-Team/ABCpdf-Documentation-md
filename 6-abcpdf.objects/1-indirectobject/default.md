---
title: "default"
css: "abcpdf-docs.css"
---

# IndirectObject Class

A PDF indirect object.

PDF supports a number of basic types of object. Objects may be labeled so that they can be referred to by other objects. This type of object is called an indirect object.

ABCpdf uses a slightly different terminology to avoid clashes with other namespaces. Objects without labels contain basic data elements and are referred to as [Atoms](../../7-abcpdf.atoms/1-atom/default.md).

The term 'indirect object' is often shortened to 'PDF object' or sometime simply 'object'. There are a variety of types of PDF objects from content layers to fonts to annotations. Every object contains an Atom which represents the data held by that object.

Indirect objects are held in an [ObjectSoup](../2-objectsoup/default.md). This is a non-traditional collection with some of the characteristics of an Array and some of a Dictionary.

``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.Annotation WebSupergoo.ABCpdf13.Objects.Bookmark WebSupergoo.ABCpdf13.Objects.Catalog WebSupergoo.ABCpdf13.Objects.ColorSpace WebSupergoo.ABCpdf13.Objects.Field WebSupergoo.ABCpdf13.Objects.FileSpecification WebSupergoo.ABCpdf13.Objects.FontObject WebSupergoo.ABCpdf13.Objects.Outline WebSupergoo.ABCpdf13.Objects.Page WebSupergoo.ABCpdf13.Objects.Pages WebSupergoo.ABCpdf13.Objects.StreamObject Implements: ICloneable, IDisposable, IEquatable ```

## Method Description S&raquo;&nbsp; FromString Construct an appropriate type of IndirectObject given a string value. IndirectObject IndirectObject Constructor. Dispose Dispose of the object. Clone Create a deep copy of the current IndirectObject. Equals Test whether the two IndirectObjects are the same. GetHashCode A hash code for the IndirectObject. Resolve Resolves any indirect references and returns the Atom. ResolveRef Resolves any indirect references and returns the final RefAtom. ResolveObj Resolves any indirect references and returns the final IndirectObject. ToString The string representation of the IndirectObject. Transcode Transcodes and reloads the IndirectObject. &nbsp;

## Property Description ID The ID of the PDF object. Gen The Generation of the PDF object. Atom The Atom contained by the IndirectObject. Version The minimum version of the PDF specification required to support this object. Revision The revision of the document in which this object is stored. Alive Whether the IndirectObject is currently alive. Doc The Doc containing this IndirectObject. Soup The soup containing this IndirectObject. AdbeExtLevel The minimum extension level of Adobe Supplement to the PDF specification required to support this object.