---
title: "01-element"
css: "abcpdf-docs.css"
---

|  |  | Element Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a new Element. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp Element() Element(Atom atom, IndirectObject host) Element(IndirectObject obj) Element(Element relation, CreationOptions options) ``` [Visual Basic] ``` Element() Element(atom As Atom, host As IndirectObject) Element(obj As IndirectObject) Element(relation As Element, options As CreationOptions) ``` `ArgumentException: Thrown if the atom is not of correct type for this type of Element.` |  |  | 
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
      
| Create a new Element. The different constructors allow different ways of creating an Element. Some are used for wrapping existing Atoms or IndirectObjects and others are for creating new ones. The constructor taking a relation Element creates a new object in the document - it is typically the constructor you will want to use. Do not specify creation options unless you have very specific needs. However for your first Element - one you can use as a relation for the others - you will need to wrap an existing IndirectObject inside an Element. For this you might use code of the following form "CatalogElement root = new CatalogElement(doc.ObjectSoup.Catalog)". The parameterless constructor allows you to create an empty Element. By empty we mean it has no contents - no Atom within it. So before use an Atom must be Assigned or Created. In practice it is easiest to do this using one of the other constructors. The atom and host constructor is used to wrap an existing Atom. It creates an Element and then Assigns the Atom to it. The result is a specialized Element which can be used to examine or modify the contents of the Atom. The CreationOptions enumeration may take the following values: Default - Default creation options for this particular type of Element. Indirect - Create Element containing an IndirectObject. Direct - Create Element containing an Atom. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This code snippet is taken from TaggedPDF.cs line 87 in the AccessiblePDF example project. [C#] ```csharp ListElement> items = new ListElement>(); FindAll(item, items); return items; ``` This code snippet is taken from Annotations.cs line 464 in the Annotations example project. [C#] ```csharp if (inKids.Count == 0) throw new Exception("Cannot have a group field with no kids"); int fieldID = Doc.AddObject(">"); FormField formField = new FormField(this, inName, fieldID, inKids); formField.FieldElement.EntryV = new Element(new StringAtom(inValue), formField.Host); return formField; ``` This code snippet is taken from Annotations.cs line 480 in the Annotations example project. [C#] ```csharp TextFieldAnnotation textField = new TextFieldAnnotation(this, inRect); FormField formField = new FormField(this, inName, textField); formField.FieldElement.EntryFT = "Tx"; formField.FieldElement.EntryFf = (int)Field.FieldFlags.Multiline; formField.FieldElement.EntryQ = 1; if (inText != null) formField.FieldElement.EntryV = new Element(new StringAtom(inText), formField.FieldElement.Host); return formField; ``` This code snippet is taken from Annotations.cs line 514 in the Annotations example project. [C#] ```csharp CheckBoxAnnotation checkBox = new CheckBoxAnnotation(this, inRect, inValue); FormField formField = new FormField(this, inName, checkBox); formField.FieldElement.EntryFT = "Btn"; formField.FieldElement.EntryV = new Element(new NameAtom(inValue ? "Yes" : "Off"), formField.Host); return formField; ``` This code snippet is taken from Annotations.cs line 529 in the Annotations example project. [C#] ```csharp List kids = new List(); for (int i = 0; i >"); FormField formField = new FormField(this, inName, fieldID, kids); formField.FieldElement.EntryV = new Element(new NameAtom(inSelectedButton.ToString()), formField.Host); return formField; ``` This code snippet is taken from Annotations.cs line 1944 in the Annotations example project. [C#] ```csharp RichMediaParamsElement pars = RichMediaElement.EntryRichMediaSettings.EntryActivation.EntryConfiguration.EntryInstances[0].EntryParams; if (string.IsNullOrEmpty(value)) pars.EntryFlashVars = null; else if (value.Length Element(new StringAtom(value), AnnotationElement.Object); else { StreamObject so = new StreamObject(Form.Doc.ObjectSoup); so.SetText(value); so.CompressFlate(); pars.EntryFlashVars = new Element(new RefAtom(so), AnnotationElement.Object); } ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>