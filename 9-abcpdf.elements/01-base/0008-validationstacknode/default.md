---
title: "default"
css: "abcpdf-docs.css"
---

# ValidationStackNode Class

StackNode class.

Validation is a recursive process. One Element validates each of its child Elements. Each of those in turn validate their children.

In the event that an inconsistency is found, it useful to know how the current Element was arrived at.

The Stack consists of a sequence of ValidationStackNode.

Each node indicates the state of validation at the point at which a child element was asked to validate itself.

There may be apparent duplicates on the stack as sub-classes may result in multiple calls to the Start function.

``` System.Object WebSupergoo.ABCpdf13.Elements.ValidationStackNode ```

## Method Description ValidationStackNode Initializes a new instance of the ValidationStackNode class. &nbsp;

## Property Description Element Gets the element to which this node refers. Entry Gets or sets the entry - the DictAtom key - which represents the current item being validated. Index Gets or sets the item - the ArrayAtom index - which represents the current item being validated.