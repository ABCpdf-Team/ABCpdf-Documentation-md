---
title: "01-catalogelement"
css: "abcpdf-docs.css"
---

|  |  | CatalogElement Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a new CatalogElement. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp CatalogElement() CatalogElement(Atom atom, IndirectObject host) CatalogElement(IndirectObject obj) CatalogElement(Element relation, CreationOptions options) ``` [Visual Basic] ``` CatalogElement() CatalogElement(atom As Atom, host As IndirectObject) CatalogElement(obj As IndirectObject) CatalogElement(relation As Element, options As CreationOptions) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The Atom to be assigned to this Element. | 
| host | An IndirectObject. This can be any IndirectObject from the Soup but ideally should be one closely associated with the Atom. | 
| obj | The IndirectObject to be assigned to this Element. | 
| relation | An Element. This can be any Element in the Soup but ideally should be one closely associated with this Element. | 
| options | Options related to creation. For example this allows you to determine whether the Element should be created using an IndirectObject rather than just an Atom. If not provided a default set of options is used. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Create a new CatalogElement. The different constructors allow different ways of creating an Element. Some are used for wrapping existing Atoms or IndirectObjects and others are for creating new ones. The constructor taking a relation Element creates a new object in the document - it is typically the constructor you will want to use. Do not specify creation options unless you have very specific needs. However for your first Element - one you can use as a relation for the others - you will need to wrap an existing IndirectObject inside an Element. For this you might use code of the following form "CatalogElement root = new CatalogElement(doc.ObjectSoup.Catalog)". The parameterless constructor allows you to create an empty Element. By empty we mean it has no contents - no Atom within it. So before use an Atom must be Assigned or Created. In practice it is easiest to do this using one of the other constructors. The atom and host constructor is used to wrap an existing Atom. It creates an Element and then Assigns the Atom to it. The result is a specialized Element which can be used to examine or modify the contents of the Atom. The CreationOptions enumeration may take the following values: Default - Default creation options for this particular type of Element. Indirect - Create Element containing an IndirectObject. Direct - Create Element containing an Atom. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This code snippet is taken from Annotations.cs line 325 in the Annotations example project. [C#] ```csharp FieldElement.EntryT = fieldName; CatalogElement cat = new CatalogElement(Form.Doc.ObjectSoup[Form.Doc.Root]); cat.EntryAcroForm.EntryFields.Add(FieldElement); ``` This code snippet is taken from Annotations.cs line 987 in the Annotations example project. [C#] ```csharp bool duplicatesFound = false; CatalogElement cat = new CatalogElement(Doc.ObjectSoup[Doc.Root]); FieldElement parent = field.FieldElement.EntryParent; InteractiveFormElement acroForm = cat.EntryAcroForm; ArrayElementFieldElement> kids = parent != null ? parent.EntryKids : acroForm.EntryFields; DictionaryFieldElement>> items = new DictionaryFieldElement>>(); foreach (var kid in kids) { if (kid == null) continue; // shouldn't really happen string name = kid.EntryT; if (!items.ContainsKey(name)) items[name] = new ListFieldElement>(); items[name].Add(kid); } foreach (KeyValuePairFieldElement>> pair in items) { if (pair.Value.Count > 1) { duplicatesFound = true; // shift field down to be a child of a new field node FieldElement newField = new FieldElement(cat); newField.EntryKids = new ArrayElementFieldElement>(acroForm); if (parent != null) { parent.EntryKids.Add(newField); newField.EntryParent = parent; } else { acroForm.EntryFields.Add(newField); } foreach (FieldElement twin in pair.Value) { if (!string.IsNullOrEmpty(twin.EntryFT)) { newField.EntryFT = twin.EntryFT; twin.EntryFT = null; } if (!string.IsNullOrEmpty(twin.EntryT)) { newField.EntryT = twin.EntryT; twin.EntryT = null; } if (!string.IsNullOrEmpty(twin.EntryTU)) { newField.EntryTU = twin.EntryTU; twin.EntryTU = null; } if (twin.EntryFf.HasValue) { newField.EntryFf = twin.EntryFf; twin.EntryFf = null; } if (twin.EntryV != null) { newField.EntryV = twin.EntryV; twin.EntryV = null; } if (twin.EntryDV != null) { newField.EntryDV = twin.EntryDV; twin.EntryDV = null; } kids.Remove(twin); newField.EntryKids.Add(twin); twin.EntryParent = newField; } } } if ((refreshForm) && (duplicatesFound)) Doc.Form.Refresh(); return duplicatesFound; ``` This code snippet is taken from ValidationUtilities.cs line 83 in the ValidatePDF example project. [C#] ```csharp ValidationLog validation = new ValidationLog(); validation.Coverage = coverage; validation.Stack = new StackValidationStackNode>(); CatalogElement cat = new CatalogElement(doc.ObjectSoup.Catalog); cat.Validate(validation); StreamObject trail = doc.ObjectSoup.Trailer; bool isCrossRef = Atom.GetItem(trail.Atom, "W") != null; CrossReferenceStreamElement crossRef = isCrossRef ? new CrossReferenceStreamElement(trail) : null; FileTrailerElement fileTrailer = !isCrossRef ? new FileTrailerElement(trail) : null; Element trailer = isCrossRef ? (Element)crossRef : (Element)fileTrailer; trailer.Validate(validation); if (doc.Encryption.Type != 0) { validation.Start(trailer); EncryptionElement encryption = crossRef != null ? crossRef.EntryEncrypt : fileTrailer.EntryEncrypt; validation.ReportEntryVersion("Encryption.V", encryption.GetEntryVersion("V")); } StringBuilder sb = validation.Log; HashSet done = validation.Done; List missed = new List(); foreach (IndirectObject io in doc.ObjectSoup) { if ((io != null) && (io.ID != 0) && (!done.Contains(io.ID))) { Element e = ElementFactories.AutodetectFactory(new RefAtom(io), io, null); if ((e is ObjectStreamElement) \|\| (e is CrossReferenceStreamElement) \|\| (e is LinearizationParameterElement)) { e.Validate(validation); done = validation.Done; } } } if (reportOrphans) { foreach (IndirectObject io in doc.ObjectSoup) { if ((io != null) && (io.ID != 0) && (!done.Contains(io.ID))) missed.Add(io); } if (missed.Count > 0) { HashSet refOnlyObjects = new HashSet(); Dictionary> references = new Dictionary>(); foreach (IndirectObject io in doc.ObjectSoup) { if (io != null) { bool hasContent = false; FindAllReferences(io.ID, io.Atom, references, ref hasContent); if (!hasContent) refOnlyObjects.Add(io.ID); } } foreach (IndirectObject io in missed) { HashSet set = null; references.TryGetValue(io.ID, out set); if (set == null) continue; // object not referenced by anything - ignore if (refOnlyObjects.Contains(io.ID)) continue; // only reference atoms - simply a stop en route to other items sb.AppendLine("Missed ID: " + io.ID.ToString() + ": " + IndirectObjectDescription(io)); foreach (var id in set) sb.AppendLine(" Referenced by ID: " + id.ToString() + ": " + IndirectObjectDescription(doc.ObjectSoup[id])); } } } string header = "PDF Version: " + GetVersion(validation.Version) + "\r\n"; if (validation.Version.HasFlag(PDFVersion.AdobeUndocumented)) header += "PDF Uses Undocumented Extensions\r\n"; if (validation.Version.HasFlag(PDFVersion.PDF20Deprecated)) { header += "PDF Uses PDF 2.0 Deprecated Features\r\n"; foreach (string feature in validation.Deprecated) header += " - " + feature + "\r\n"; } header += "\r\n"; return header + sb.ToString(); ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>