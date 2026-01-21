---
title: "default"
css: "abcpdf-docs.css"
---

# DrawPagesOperation Class

Operation to draw pages from one document onto another.

This operation is in many ways similar to the Doc.AddImageDoc function. However the AddImageDoc function is not aware of state and thus it has to take each call afresh.

In contrast the DrawPagesOperation is aware of state which means that, for a process drawing many pages between two documents, it can operate much more quickly.

It also means it can factor out duplicate resources more effectively. So document level structures like optional content group - OCG - layers can be represented more efficiently rather than being repeated for each page added.

``` System.Object WebSupergoo.ABCpdf13.Operations.DrawPagesOperation ```

`Implements: IDisposable`

## Method Description DrawPagesOperation DrawPagesOperation constructor. DrawPage Draw the current page from the source to the destination document. &nbsp;

## Property Description Source The source document from which to take pages. Destination The destination document onto which pages will be drawn. CopyAnnotations Whether to copy fields and annotations. CopyTags Whether to copy accessibility tags. UseSourceRect Whether to draw only the portion of the page specified by the Souce. Alpha The level of alpha to apply to the drawn page. RootTag The root structure element for the added tags.