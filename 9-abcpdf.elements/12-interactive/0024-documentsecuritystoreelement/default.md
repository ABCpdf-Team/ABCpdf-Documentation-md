# DocumentSecurityStoreElement Class

This class represents the document security store dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 261, page 582.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because SignatureValidationRelatedInformationElement.EntryCRL and SignatureValidationRelatedInformationElement.EntryOCSP require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.DocumentSecurityStoreElement ```

## Method Description DocumentSecurityStoreElement Create a new DocumentSecurityStoreElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the document security store dictionary object. EntryVRI Represents the "VRI" entry of the document security store dictionary object. EntryCerts Represents the "Certs" entry of the document security store dictionary object. EntryOCSPs Represents the "OCSPs" entry of the document security store dictionary object. EntryCRLs Represents the "CRLs" entry of the document security store dictionary object. inherited properties...