---
title: "default"
css: "abcpdf-docs.css"
---

# AccessibilityOperation Class

Operation to make a document accessible.

Accessible or Tagged PDFs are the same as normal PDFs but have been annotated with metadata in the form of PDF tags. This metadata is required because PDF documents contain good layout information but little semantic structure. The tags that are required supply this semantic structure. The way they are inserted and operate is defined in the Adobe PDF Specification.

See the [MakeAccessible](1-methods/makeaccessible.md) function for further information on accessibility standards and tagged PDF.

``` System.Object WebSupergoo.ABCpdf13.Operations.AccessibilityOperation ```

## Method Description &nbsp;AccessibilityOperation AccessibilityOperation Constructor. &nbsp;MakeAccessible Tags the document for accessibility. &nbsp;

## Property Description PageContents The pages to be operated upon. ActualText Whether to embed the actual text of text elements. FixFonts Whether to attempt to fix font settings that may be required for accessibility. FixMetadata Whether to attempt to fix or add metadata that may be required for accessibility. FindHeaders Whether to detect and remove page headers. FindFooters Whether to detect and remove page footers. FindLists Whether to detect and insert ordered and unordered list structures. FindStructure Whether to detect and insert structure outline. FindTables Whether to detect and insert table structures. Layout The method that should be used for determining paragraph order. TextOperation The text analysis operation for the accessibility analysis.