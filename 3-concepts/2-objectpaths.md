# Object Paths

Adobe Portable Document Format (PDF) files are made of a number of objects. Objects may describe a page, a resource, a sequence of drawing operations an image or many other components as required by the document.

Every object has a unique Object ID numbered from one upwards. The ID zero refers to the Empty Object which is an object required internally within ABCpdf. ID -1 refers to the document trailer. The root of the document hierarchy can be accessed using the Doc.Root property or the ObjectSoup.Catalog.

You can use the GetInfo and SetInfo methods to directly manipulate any PDF object in your document. However, this is not advisable unless you are reasonably familiar with the Adobe PDF Specification.

Under normal situations, ABCpdf ensures that your documents are internally consistent. Using the SetInfo method with Dictionaries, Values or Paths allows great flexibility in modifying documents but also allows you to create invalid or corrupt documents.

If your object is a dictionary, you can specify a particular dictionary entry for replacement or insertion (dictionary entries always begin with a slash '/' character). So if you wanted to change the type of an annotation, you might use the following code:

[C#] theDoc.SetInfo(theID, "/Subtype", "(Stamp)");

Alternatively, you can use the 'Value' selector to specify a replacement for the entire object. However, if you do this, you must ensure that the type of your new object is the same as the type of your old one - you cannot replace a number with a string. For example.

[C#] theDoc.SetInfo(theID, "Value", "<</Font /Helvetica /Size 10>>");

Specifications can be chained together to form complete paths. Dictionary entries are specified by preceding the entry name with a slash. Array items are specified using square brackets containing the index of the item you wish to reference (starting at zero).

For example, the code below would return the first item in the MediaBox array.

[C#] theDoc.GetInfo(theID, "/MediaBox[0]");

And the code below would return the count entry of the parent of the object.

[C#] theDoc.GetInfo(theID, "/Parent/Count");

Sometimes, you may wish to find a reference to a particular object. Sometimes, you may wish to skip through the reference and jump straight into the object itself.

You can do this using an asterisk to de-reference an object within a path. If the object is a reference, it will be de-referenced; if it is not, then the operator will be ignored.

For example, the code below might be used to return the content stream of the first page of a document.

[C#] theDoc.GetInfo(theDoc.Root, "/Pages*/Kids*[0]*/Contents");

You can use SetInfo to insert values specified by paths. You can specify the type of object to be inserted by appending an identifier to the path.

A Boolean value.

A name value.

A numeric value

A string value.

An indirect reference to an object.

A rectangle. Internally, rectangles are held as arrays of numbers, but this provides a convenient shortcut.

This is a special entry. It does not insert an object. Instead, it ensures that the object specified by the path is deleted.

The asterisk is a delimiter. Each of 'Hex', 'NoBreak', and 'Byte' is optional. For example, you can specify "/MyEntry:Text[Hex]".

The 'Hex' specifier indicates that the text should be hex-encoded. The 'NoBreak' specifier indicates that there should be no line breaks. Also available is the 'Byte' specifier, which indicates that characters should be interpreted as a string of bytes rather than a Unicode string. These settings are used infrequently, and in general, you will not need them.

This only works for string atoms.

If the string atom contains a value it returns that value.

If there is no value, or the atom is of the wrong type, it returns the special string.

"string_is_null\0ABCpdf"

The number in 32 bit integer format.

It may not be possible to represent a value in this format if the number has a floating point element or is too big or too small.

If it is not possible to represent the value, a default value of zero is returned.

The equivalent of Int32 but for 64 bit integer values.

The equivalent of Int32 but specifying a default value of -1.

The equivalent of Int64 but specifying a default value of -1.

Suppose you wanted to insert an annotation into the page annotations array. The following code will find the page entry named "/Annots" (or it will create it if it doesn't exist). It will then ensure that this entry references an array, and it will insert a reference Atom at the beginning (item zero) of the array.

[C#] theDoc.SetInfo(theDoc.Page, "/Annots[0]:Ref", theID);

Alternatively, if you want to insert your annotation at the end of the array, just leave out the array index:

[C#] theDoc.SetInfo(theDoc.Page, "/Annots[]:Ref", theID);

You can also locate items in an array from the end. Use -1 for the last item, -2 for the second last item, and so on.

[C#] theDoc.GetInfo(theDoc.Page, "/Annots[-1]:Ref");

Insertions can be complex. The next example gets the entry called "/Font", which contains a dictionary. This dictionary includes an element called "/Names", which contains an array. The call inserts the Name object "/Helvetica" at the start of this array.

[C#] theDoc.SetInfo(theID, "/Font/Names[0]:Name", "Helvetica");

You can use GetInfo to query values specified by paths. The format of the return value is exactly the same as would be output to your PDF file. You can specify an alternative format by appending an identifier to the string.

The Object ID associated with an object reference.

Normally, object references are returned in an extended format (e.g. 23 0 R ). However, if you are only interested in the Object ID, then you use this format specifier to get only the Object ID (e.g. 23 ).

The object value.

This is used to ensure that all indirect references are resolved before the value of the object is returned. This ensures you always get an object value rather than an object reference.

The text of a name or string.

Names and strings may be encoded in a number of ways before output to PDF. The text format specifier ensures that the unencoded value is returned.

The value of a number.

If the object referred to is not a number, then no value is returned.

The rect string for a rectangle object.

Rects are typically represented as an array. By specifying the rect format, you will get a string value you can place directly into the XRect object.

The number of items in an array.

The count specifier is a special directive which returns the number of items in an array rather than an item from that array.

The number of items in a dictionary.

The keycount specifier is a special directive which returns the number of items in a dictionary rather than an item from that dictionary.

The keys for a dictionary.

The keys specifier is a special directive which returns a comma delimited list of the names of the entries in the dictionary.

For example, the code below could return the rect of the page CropBox.

[C#] theDoc.GetInfo(theID, "/CropBox:Rect");

