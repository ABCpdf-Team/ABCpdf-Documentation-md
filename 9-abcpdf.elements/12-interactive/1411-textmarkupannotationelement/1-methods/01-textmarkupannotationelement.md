---
title: "01-textmarkupannotationelement"
css: "abcpdf-docs.css"
---

|  |  | TextMarkupAnnotationElement Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Create a new TextMarkupAnnotationElement. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp TextMarkupAnnotationElement() TextMarkupAnnotationElement(Atom atom, IndirectObject host) TextMarkupAnnotationElement(IndirectObject obj) TextMarkupAnnotationElement(Element relation, CreationOptions options) ``` [Visual Basic] ``` TextMarkupAnnotationElement() TextMarkupAnnotationElement(atom As Atom, host As IndirectObject) TextMarkupAnnotationElement(obj As IndirectObject) TextMarkupAnnotationElement(relation As Element, options As CreationOptions) ``` |  |  | 
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
      
| Create a new TextMarkupAnnotationElement. The different constructors allow different ways of creating an Element. Some are used for wrapping existing Atoms or IndirectObjects and others are for creating new ones. The constructor taking a relation Element creates a new object in the document - it is typically the constructor you will want to use. Do not specify creation options unless you have very specific needs. However for your first Element - one you can use as a relation for the others - you will need to wrap an existing IndirectObject inside an Element. For this you might use code of the following form "CatalogElement root = new CatalogElement(doc.ObjectSoup.Catalog)". The parameterless constructor allows you to create an empty Element. By empty we mean it has no contents - no Atom within it. So before use an Atom must be Assigned or Created. In practice it is easiest to do this using one of the other constructors. The atom and host constructor is used to wrap an existing Atom. It creates an Element and then Assigns the Atom to it. The result is a specialized Element which can be used to examine or modify the contents of the Atom. The CreationOptions enumeration may take the following values: Default - Default creation options for this particular type of Element. Indirect - Create Element containing an IndirectObject. Direct - Create Element containing an Atom. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This code snippet is taken from Annotations.cs line 1746 in the Annotations example project. [C#] ```csharp TextMarkupAnnotationElement annot = new TextMarkupAnnotationElement(AnnotationElement.Object); annot.EntrySubtype = markupType; annot.EntryQuadPoints = Array.ConvertAll(quadPoints.Split(new char[] { ' ' }), s => double.Parse(s, NumberFormatInfo.InvariantInfo)); AnnotationElement = annot; Color = color; ``` This code snippet is taken from Annotations.cs line 1767 in the Annotations example project. [C#] ```csharp XRect rect = new XRect(Form.Doc.GetInfo(id, "Rect")); TextMarkupAnnotationElement annot = new TextMarkupAnnotationElement(AnnotationElement.Object); annot.EntrySubtype = markupType; annot.EntryQuadPoints = new double[] { rect.Left, rect.Top, rect.Right, rect.Top, rect.Left, rect.Bottom, rect.Right, rect.Bottom }; annot.EntryRect = new RectangleElement(ArrayAtom.FromXRect(rect), annot.Host); AnnotationElement = annot; Color = color; ``` This code snippet is taken from Annotations.cs line 1784 in the Annotations example project. [C#] ```csharp XRect rect = Form.Doc.Rect; TextMarkupAnnotationElement annot = new TextMarkupAnnotationElement(AnnotationElement.Object); annot.EntrySubtype = markupType; annot.EntryQuadPoints = new double[] { rect.Left, rect.Top, rect.Right, rect.Top, rect.Left, rect.Bottom, rect.Right, rect.Bottom }; annot.EntryRect = new RectangleElement(ArrayAtom.FromXRect(rect), annot.Host); AnnotationElement = annot; Color = color; ``` |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>