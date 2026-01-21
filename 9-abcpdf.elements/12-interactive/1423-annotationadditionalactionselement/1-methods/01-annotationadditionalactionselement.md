---
title: "01-annotationadditionalactionselement"
css: "abcpdf-docs.css"
---

|  |  | AnnotationAdditionalActionsElement Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a new AnnotationAdditionalActionsElement. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp AnnotationAdditionalActionsElement() AnnotationAdditionalActionsElement(Atom atom, IndirectObject host) AnnotationAdditionalActionsElement(IndirectObject obj) AnnotationAdditionalActionsElement(Element relation, CreationOptions options) ``` [Visual Basic] ``` AnnotationAdditionalActionsElement() AnnotationAdditionalActionsElement(atom As Atom, host As IndirectObject) AnnotationAdditionalActionsElement(obj As IndirectObject) AnnotationAdditionalActionsElement(relation As Element, options As CreationOptions) ``` |  |  | 
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
      
| Create a new AnnotationAdditionalActionsElement. The different constructors allow different ways of creating an Element. Some are used for wrapping existing Atoms or IndirectObjects and others are for creating new ones. The constructor taking a relation Element creates a new object in the document - it is typically the constructor you will want to use. Do not specify creation options unless you have very specific needs. However for your first Element - one you can use as a relation for the others - you will need to wrap an existing IndirectObject inside an Element. For this you might use code of the following form "CatalogElement root = new CatalogElement(doc.ObjectSoup.Catalog)". The parameterless constructor allows you to create an empty Element. By empty we mean it has no contents - no Atom within it. So before use an Atom must be Assigned or Created. In practice it is easiest to do this using one of the other constructors. The atom and host constructor is used to wrap an existing Atom. It creates an Element and then Assigns the Atom to it. The result is a specialized Element which can be used to examine or modify the contents of the Atom. The CreationOptions enumeration may take the following values: Default - Default creation options for this particular type of Element. Indirect - Create Element containing an IndirectObject. Direct - Create Element containing an Atom. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This code snippet is taken from Annotations.cs line 1584 in the Annotations example project. [C#] ```csharp bool isUrl = filePathOrUrl.StartsWith("http://", StringComparison.OrdinalIgnoreCase) \|\| filePathOrUrl.StartsWith("https://", StringComparison.OrdinalIgnoreCase) \|\| filePathOrUrl.StartsWith("rtmp://", StringComparison.OrdinalIgnoreCase); if (contentType == null) { int end = -1; if (isUrl) end = filePathOrUrl.IndexOfAny(new char[] { '?', '#' }); if (end ScreenAnnotationElement annot = new ScreenAnnotationElement(AnnotationElement.Object); annot.EntrySubtype = "Screen"; annot.EntryRect = new RectangleElement(ArrayAtom.FromXRect(new XRect(rect)), annot.Host); FullFileSpecificationElement fileSpec = new FullFileSpecificationElement(annot); fileSpec.EntryType = "Filespec"; if (isUrl) { fileSpec.EntryFS = "URL"; fileSpec.EntryF = filePathOrUrl; } else { FileInfo fileInfo = new FileInfo(filePathOrUrl); fileSpec.EntryF = fileInfo.Name; fileSpec.EntryUF = fileInfo.Name; fileSpec.EntryEF = new EmbeddedFileSetElement(annot); fileSpec.EntryEF.EntryF = EmbedFileStream(fileInfo); } MediaClipDataElement mediaClip = new MediaClipDataElement(annot, CreationOptions.Indirect); mediaClip.EntryS = "MCD"; mediaClip.EntryP = new MediaPermissionsElement(annot); mediaClip.EntryP.EntryTF = "TEMPACCESS"; mediaClip.EntryCT = contentType; mediaClip.EntryD = fileSpec; MediaRenditionElement rendition = new MediaRenditionElement(annot, CreationOptions.Indirect); rendition.EntryS = "MR"; rendition.EntryC = mediaClip; RenditionActionElement pageVisibleAction = new RenditionActionElement(annot, CreationOptions.Indirect); pageVisibleAction.EntryS = "Rendition"; pageVisibleAction.EntryOP = 4; pageVisibleAction.EntryAN = annot; pageVisibleAction.EntryR = rendition; annot.EntryAA = new AnnotationAdditionalActionsElement(annot); annot.EntryAA.EntryPV = pageVisibleAction; AnnotationElement = annot; ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>