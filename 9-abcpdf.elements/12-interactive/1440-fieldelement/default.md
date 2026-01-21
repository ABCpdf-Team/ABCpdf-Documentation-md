# FieldElement Class

This class represents the field dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 220, page 432.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=440)

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 222, page 434.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=442)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 226, page 527.](https://www.iso.org/standard/63534.md)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 228, page 529.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because FDFFieldElement.EntryKids, FDFTemplateElement.EntryFields, FieldElement.EntryKids, InteractiveFormElement.EntryCO, InteractiveFormElement.EntryFields, ResetFormActionElement.EntryFields, SubmitFormActionElement.EntryFields and WidgetAnnotationElement.EntryParent require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.FieldElement WebSupergoo.ABCpdf13.Elements.CheckboxFieldElement WebSupergoo.ABCpdf13.Elements.ComboFieldElement WebSupergoo.ABCpdf13.Elements.ListFieldElement WebSupergoo.ABCpdf13.Elements.PushbuttonFieldElement WebSupergoo.ABCpdf13.Elements.RadioFieldElement WebSupergoo.ABCpdf13.Elements.SignatureFieldElement WebSupergoo.ABCpdf13.Elements.TextFieldElement ```

## Method Description FieldElement Create a new FieldElement. inherited methods... &nbsp;

## Property Description WidgetAnnotationElement Any WidgetAnnotationElement associated with this Field. EntryFT Represents the "FT" entry of the field dictionary object. EntryParent Represents the "Parent" entry of the field dictionary object. EntryKids Represents the "Kids" entry of the field dictionary object. EntryT Represents the "T" entry of the field dictionary object. EntryTU Represents the "TU" entry of the field dictionary object. EntryTM Represents the "TM" entry of the field dictionary object. EntryFf Represents the "Ff" entry of the field dictionary object. EntryV Represents the "V" entry of the field dictionary object. EntryDV Represents the "DV" entry of the field dictionary object. EntryAA Represents the "AA" entry of the field dictionary object. EntryDA Represents the "DA" entry of the field dictionary object. EntryQ Represents the "Q" entry of the field dictionary object. EntryDS Represents the "DS" entry of the field dictionary object. EntryRV Represents the "RV" entry of the field dictionary object. EntryOpt Represents the "Opt" entry of the field dictionary object. EntryMaxLen Represents the "MaxLen" entry of the field dictionary object. inherited properties...