---
title: "01-arrayelement_t_"
css: "abcpdf-docs.css"
---

# ArrayElement&lt;T&gt; Function

Create a new [ArrayElement](../default.md).

## Syntax

**[C#]**

```csharp
ArrayElement()
ArrayElement(Atom atom, IndirectObject host)
ArrayElement(IndirectObject obj)
ArrayElement(Element relation, CreationOptions options)
```

<span class=language>[Visual Basic]</span>  

```
ArrayElement()
ArrayElement(atom As Atom, host As IndirectObject)
ArrayElement(obj As IndirectObject)
ArrayElement(relation As Element, options As CreationOptions)
```

## Params

| Name | Description | 
| --- | --- |
| atom | The Atom to be assigned to this Element. | 
| host | An IndirectObject. This can be any IndirectObject from the Soup but ideally should be one closely associated with the Atom. | 
| obj | The IndirectObject to be assigned to this Element. | 
| relation | An Element. This can be any Element in the Soup but ideally should be one closely associated with this Element. | 
| options | Options related to creation. For example this allows you to determine whether the Element should be created using an IndirectObject rather than just an Atom. If not provided a default set of options is used. | 

## Notes

Create a new [ArrayElement](../default.md).

The different constructors allow different ways of creating an [Element](../../1086-element/default.md). Some are used for wrapping existing Atoms or IndirectObjects and others are for creating new ones.

The constructor taking a relation [Element](../../1086-element/default.md) creates a new object in the document - it is typically the constructor you will want to use. Do not specify creation options unless you have very specific needs.

However for your first [Element](../../1086-element/default.md) - one you can use as a relation for the others - you will need to wrap an existing IndirectObject inside an [Element](../../1086-element/default.md). For this you might use code of the following form "[CatalogElement](../../../07-syntax/1081-catalogelement/default.md) root = new [CatalogElement](../../../07-syntax/1081-catalogelement/default.md)(doc.ObjectSoup.Catalog)".

The parameterless constructor allows you to create an empty [Element](../../1086-element/default.md). By empty we mean it has no contents - no Atom within it. So before use an Atom must be Assigned or Created. In practice it is easiest to do this using one of the other constructors.

The atom and host constructor is used to wrap an existing Atom. It creates an [Element](../../1086-element/default.md) and then Assigns the Atom to it. The result is a specialized [Element](../../1086-element/default.md) which can be used to examine or modify the contents of the Atom.

The CreationOptions enumeration may take the following values:

- Default - Default creation options for this particular type of [Element](../../1086-element/default.md).
- Indirect - Create [Element](../../1086-element/default.md) containing an IndirectObject.
- Direct - Create [Element](../../1086-element/default.md) containing an Atom.

## Example

This code snippet is taken from TaggedPDF.cs line 630 in the AccessiblePDF example project.

[C#]

```csharp
if (parent.EntryK == null)
  parent.EntryK = new ArrayElementElement>(parent);
if (index > parent.EntryK.Count)
  index = parent.EntryK.Count;
parent.EntryK.Insert(index, element);
```

This code snippet is taken from Annotations.cs line 81 in the Annotations example project.

[C#]

```csharp
BorderStyleElement.EntryD = new ArrayElementElement>(Atom.FromString(value), AnnotationElement.Host);
```

This code snippet is taken from Annotations.cs line 310 in the Annotations example project.

[C#]

```csharp
string partialName, parentName;
List parts = new List(fieldName.Split(new char[] { '.' }));
partialName = parts[parts.Count - 1];
if (string.IsNullOrEmpty(parts[parts.Count - 1]))
  parts.RemoveAt(parts.Count - 1);
parentName = string.Join(".", parts);
FieldElement parent = new FieldElement(Form.Doc.Form[parentName]);
if (parent.EntryKids == null)
  parent.EntryKids = new ArrayElementFieldElement>();
parent.EntryKids.Add(FieldElement);
FieldElement.EntryParent = parent;
if (!string.IsNullOrEmpty(partialName))
  FieldElement.EntryT = fieldName;
```

This code snippet is taken from Annotations.cs line 333 in the Annotations example project.

[C#]

```csharp
int fieldID = FieldElement.Object.ID;
if ((Widgets.Count == 0) || ((Widgets.Count == 1) && (Widgets[0].AnnotationElement.Object.ID == fieldID))) {
  FieldElement.EntryKids = null;
  return;
}
FieldElement.EntryKids = new ArrayElementFieldElement>(FieldElement);
string ft = null;
Element dv = null;
foreach (WidgetAnnotation widget in Widgets) {
  FieldElement kid = new FieldElement(widget.WidgetElement.Object);
  if (kid.Object.ID != fieldID) { // not the same object
    kid.EntryParent = FieldElement;
    FieldElement.EntryKids.Add(kid);
  }
  if (ft == null)
    ft = kid.EntryFT;
  if (dv == null)
    dv = kid.EntryDV;
  kid.EntryFT = null;
  kid.EntryV = null;
  kid.EntryDV = null;
}
if (ft != null)
  FieldElement.EntryFT = ft;
if (dv != null)
  FieldElement.EntryDV = dv;
```

<p>