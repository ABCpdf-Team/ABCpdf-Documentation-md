# XForm Object

Represents the form and fields associated with this document.

The PDF specification makes a distinction between a field (in terms of a named value) and the visible appearance of the field on the document.

In general one field will have one visible appearance on the document. However it is possible for a field to have multiple or indeed no appearances on the document.

For example a Radio Button group encapsulates one value and is represented by one field. However each radio button has a separate appearance on the document. So one Radio Button field is likely to have many appearances.

For this reason fields exist within a hierarchy. Each field may or may not have a visible appearance. Each field may or may not have children. These children may be fields themselves and again may have their own children.

Fields are generally referenced by fully qualified name. A full name describes a path down through the field hierarchy - using periods as delimiters - to a specific field object. For example the name 'person.address.city' would reference a field with a partial field name called 'city' which has a parent called 'address' which has a parent at the top level called 'person'. You can resolve a fully qualified name using the[Item](1-methods/item.md) function.

Once a field has been obtained you can query or change its values. If you wish to convert the fields into a permanent part of the document you can use the [Stamp](1-methods/stamp.md) method to permanently emboss them.

``` System.Object WebSupergoo.ABCpdf13.XForm ```

## Method Description AddComboBoxField Add combo box form field. AddListBoxField Add list box form field. AddGroupField Add group field. AddTextField Add text field. AddButton Add button field. AddCheckbox Add check box form field. AddRadioButtonGroup Add radio button group. AddResource Add a particular type of resource to the form. AddSignature Add unsigned signature field. AddDocTimestamp Adds a Signature field compatible with a document timestamp. Create Create an AcroForm if one does not already exist. GetFieldNames Gets the full names of all the fields in the document. Item Gets or sets a particular field referenced by full name. MakeFieldIntoGroup Make duplicate fields into synchronized groups. MakeFieldsUnique Makes shared XForm fields unique. Remove Remove a field from the form. RunJS Run JavaScript code. Stamp Stamp all fields into the document. &nbsp;

## Property Description DateTimeFormat The format provider for formatting dates and times. Fields All top level fields in the form. FormatFields Whether values should be formatted before insertion into fields. GenerateAppearances Whether field appearances should be pre-generated. NeedAppearances Whether the viewer should automatically regenerate field appearances. UseFieldScript Whether the viewer should run JavaScript field calculations.