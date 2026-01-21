---
title: "default"
css: "abcpdf-docs.css"
---

# ProcessingObjectEventArgs Class

Provides data for the [ProcessingObject](../1-operation/3-events/1-processingobject.md) event.

This class inherits from the CancelEventArgs class to allow processing of the operation to be cancelled.

``` System.Object System.EventArgs System.ComponentModel.CancelEventArgs WebSupergoo.ABCpdf13.Operations.ProcessingObjectEventArgs ```

## Method Description ProcessingObjectEventArgs ProcessingObjectEventArgs Constructor. &nbsp;

## Property Description Object Gets the IndirectObject to be processed. Tag Gets or sets an object which can be used to save data about the event. Info Gets the ProcessingInfo containing related information.