# StructureElementElement Function

Create a new [StructureElementElement](../default.md).

## Syntax

**[C#]**

```csharp
StructureElementElement()
StructureElementElement(Atom atom, IndirectObject host)
StructureElementElement(IndirectObject obj)
StructureElementElement(Element relation, CreationOptions options)
```

<span class=language>[Visual Basic]</span>  

```
StructureElementElement()
StructureElementElement(atom As Atom, host As IndirectObject)
StructureElementElement(obj As IndirectObject)
StructureElementElement(relation As Element, options As CreationOptions)
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

Create a new [StructureElementElement](../default.md).

The different constructors allow different ways of creating an [Element](../../../01-base/1086-element/default.md). Some are used for wrapping existing Atoms or IndirectObjects and others are for creating new ones.

The constructor taking a relation [Element](../../../01-base/1086-element/default.md) creates a new object in the document - it is typically the constructor you will want to use. Do not specify creation options unless you have very specific needs.

However for your first [Element](../../../01-base/1086-element/default.md) - one you can use as a relation for the others - you will need to wrap an existing IndirectObject inside an [Element](../../../01-base/1086-element/default.md). For this you might use code of the following form "[CatalogElement](../../../07-syntax/1081-catalogelement/default.md) root = new [CatalogElement](../../../07-syntax/1081-catalogelement/default.md)(doc.ObjectSoup.Catalog)".

The parameterless constructor allows you to create an empty [Element](../../../01-base/1086-element/default.md). By empty we mean it has no contents - no Atom within it. So before use an Atom must be Assigned or Created. In practice it is easiest to do this using one of the other constructors.

The atom and host constructor is used to wrap an existing Atom. It creates an [Element](../../../01-base/1086-element/default.md) and then Assigns the Atom to it. The result is a specialized [Element](../../../01-base/1086-element/default.md) which can be used to examine or modify the contents of the Atom.

The CreationOptions enumeration may take the following values:

- Default - Default creation options for this particular type of [Element](../../../01-base/1086-element/default.md).
- Indirect - Create [Element](../../../01-base/1086-element/default.md) containing an IndirectObject.
- Direct - Create [Element](../../../01-base/1086-element/default.md) containing an Atom.

## Example

This code snippet is taken from Form1.cs line 294 in the AccessiblePDF example project.

[C#]

```csharp
if (table.Items.Count StructureElementElement parent = null;
StructureElementElement tb = new StructureElementElement(document);
tb.EntryType = "StructElem";
tb.EntryS = "Table";
foreach (Row row in table.Items) {
  StructureElementElement tr = new StructureElementElement(document);
  tr.EntryType = "StructElem";
  tr.EntryS = "TR";
  tr.SetParent(tb);
  foreach (StructureElementElement item in row.Items) {
    if ((parent == null) && (item != null)) {
      Debug.Assert(item.EntryP is StructureTreeRootElement == false);
      parent = item.EntryP as StructureElementElement;
      index = parent.EntryK.IndexOf(item);
    }
    StructureElementElement td = new StructureElementElement(document);
    td.EntryType = "StructElem";
    td.EntryS = "TD";
    td.SetParent(tr);
    if (item != null)
      item.SetParent(td);
  }
}
tb.SetParent(parent, index);
```

This code snippet is taken from Form1.cs line 335 in the AccessiblePDF example project.

[C#]

```csharp
theDoc.Read(src);
AccessibilityOperation op = new AccessibilityOperation(theDoc);
op.PageContents.AddPages();
op.MakeAccessible();
theDoc.Save(dst);
Structure tags = new Structure();
tags.Load(theDoc);
// reorder elements so that they go from top to bottom
StructureElementElement document = (StructureElementElement)tags.Root.EntryK[0];
KidArranger.SortTopToBottom(tags, document);
// determine what styles are used for headers and change tag type appropriately
ListStructureElementElement> elements = tags.FindElementsByType("P");
DictionaryStructureElementElement>> styles = new DictionaryStructureElementElement>>();
foreach (StructureElementElement element in elements) {
  string weight = null;
  if (!element.GetStyle().TryGetValue("font-weight", out weight))
    continue; // we are only interested in bold fonts
  int value = 0;
  if ((!int.TryParse(weight, out value)) || (value StructureElementElement> matches = null;
  if (!styles.TryGetValue(size, out matches)) {
    matches = new ListStructureElementElement>();
    styles[size] = matches;
  }
  matches.Add(element);
}
List headers = new List();
foreach (KeyValuePairStructureElementElement>> pair in styles)
  headers.Add(new Style(pair.Key, pair.Value));
headers.Sort((i1, i2) => i1.Elements.Count.CompareTo(i2.Elements.Count));
for (int i = 0; i  4)
    break; // limit the number of header levels
  string tag = "H" + (i + 1).ToString();
  foreach (StructureElementElement element in headers[i].Elements) {
    element.EntryS = tag;
  }
}
theDoc.Save(dst);
```

This code snippet is taken from Form1.cs line 406 in the AccessiblePDF example project.

[C#]

```csharp
list = new StructureElementElement(document);
list.EntryType = "StructElem";
list.EntryS = "L";
Debug.Assert(element.EntryP is StructureTreeRootElement == false);
StructureElementElement parent = element.EntryP as StructureElementElement;
Debug.Assert(parent != null);
int index = parent.EntryK.IndexOf(element);
list.SetParent(parent, index);
```

This code snippet is taken from Form1.cs line 435 in the AccessiblePDF example project.

[C#]

```csharp
theDoc.Read(src);
AccessibilityOperation op = new AccessibilityOperation(theDoc);
op.PageContents.AddPages();
op.MakeAccessible();
theDoc.Save(dst);
Structure tags = new Structure();
tags.Load(theDoc);
// reorder elements so that they go from top to bottom
StructureElementElement document = (StructureElementElement)tags.Root.EntryK[0];
KidArranger.SortTopToBottom(tags, document);
// define structure hierarchy template
List template = new List();
template.Add(new Heading("Title ", "Part", 1));
template.Add(new Heading("Subheader ", "Sect", 2));
// detect and insert section item structure
ListStructureElementElement> elements = tags.FindElementsByType("P");
StackStructureElementElement> hierarchy = new StackStructureElementElement>();
foreach (StructureElementElement element in elements) {
  string text = element.EntryActualText.TrimStart();
  foreach (Heading item in template) {
    if (text.StartsWith(item.Match)) {
      while (hierarchy.Count >= item.Level)
        hierarchy.Pop();
      if (hierarchy.Count == item.Level - 1) {
        StructureElementElement heading = new StructureElementElement(document);
        heading.EntryType = "StructElem";
        heading.EntryS = item.Type;
        StructureElementElement parent = (StructureElementElement)element.EntryP;
        int index = parent.EntryK.IndexOf(element);
        heading.SetParent(hierarchy.Count > 0 ? hierarchy.Peek() : parent, index);
        hierarchy.Push(heading);
      }
      break;
    }
  }
  if (hierarchy.Count > 0)
    element.SetParent(hierarchy.Peek(), Int32.MaxValue);
}
theDoc.Save(dst);
```

This code snippet is taken from TableDetection.cs line 171 in the AccessiblePDF example project.

[C#]

```csharp
_tags = tags;
_items = new ListStructureElementElement>();
```

This code snippet is taken from TaggedPDF.cs line 61 in the AccessiblePDF example project.

[C#]

```csharp
_root = new StructureElementElement(root, _catalog);
DictAtom tree = _catalog.Resolve(Atom.GetItem(_root.Atom, "ParentTree")) as DictAtom;
_parentTree = new ParentTree(this, tree);
```

This code snippet is taken from TaggedPDF.cs line 69 in the AccessiblePDF example project.

[C#]

```csharp
ListStructureElementElement> items = new ListStructureElementElement>();
FindElementsByType(_root, items, type);
return items;
```

<p>