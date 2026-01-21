# FileSpecification Class

A file specification represents the name and location of a file and optionally may also include references to embedded data.

The crucial properties of this class are Uri and EmbeddedFile. All other methods and properties are organized around backwards compatibility with obsolete entries so you are unlikely to need them when constructing new documents..

If you have an old PDF which contains obsolete entries, the Rationalize method will attempt to make the entries compliant. So again you should only need the Rationalize method and the Uri and EmbeddedFile properties.

``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.FileSpecification ```

## Method Description FileSpecification FileSpecification Constructor. GetPath Get the path to the file for the specified platform. Rationalize Removes any obsolescent and redundant entries. SetPath Set the path to the file for the specified platform. &nbsp;

## Property Description Description A description of the file for use in a user interface. EmbeddedFile The embedded file if one has been embedded in the PDF. EmbeddedFiles The set of embedded files if a set has been embedded in the PDF. Platform The default platform being used for the file specification. &nbsp;Uri The URI to the file. Volatile Whether the file changes frequently.