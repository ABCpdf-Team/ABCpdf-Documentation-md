# CompressObjects Property

## Notes

This property determines if object stream compression should be used.

Object stream compression allows groups of simple atoms to be stored in a separate stream (an ObjStm) and compressed. This can reduce the output file size.

Typically the PDF specification is efficiently organized, atoms are small and not many are required. Thus the overhead associated with uncompressed atoms is typically minimal. Since not all PDF readers support object streams we default to avoiding this type of structure. In particular, older versions of Acrobat (eg 8) are not happy reading documents which incorporate both object streams and linearized content.

In a few cases the PDF specification has not been efficiently organized. The most notable situation in which this occurs is in the case of Tagged PDF - often required for accessibility. The structures required for tagging can result in a multitude of similar atoms and using object stream compression can make a significant difference to the size of output. It is perhaps notable that tagged PDF was introduced in PDF 1.4 and then object streams were introduced immediately afterwards in PDF 1.5. File size reduction will vary considerably depending on content but 10% might be typical.

The other situation in which this option can make a notable difference is in the case of very small PDF documents. In documents measuring ten or twenty kilobytes, atoms can make up a significant proportion of the document size. In these situations you might be able to reduce the size by perhaps 30% simply by enabling this option.

In addition to reducing the size of the document, setting this property allows you to save PDF files greater than 10GB in size.

Object stream compression is incompatible with Incremental update. If this flag is set then object stream compression will not be used.

Future Changes. As PDF documents become more accessible there may be more reason to apply object stream compression. Similarly as PDF readers improve there may be less reason not to use it. As such it is possible that the default value of this property might be changed. If you are relying on a particular value you should set it in your code.

## Example

None.

