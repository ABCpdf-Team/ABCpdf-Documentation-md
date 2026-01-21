---
title: "02-assign"
css: "abcpdf-docs.css"
---

|  |  | Assign Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Assign an IndirectObject to this Element. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual bool Assign(IndirectObject obj) virtual bool Assign(Atom host, IndirectObject atom) ``` [Visual Basic] ``` Overridable Function Assign(obj As IndirectObject) As Boolean Overridable Function Assign(host As Atom, atom As IndirectObject) As Boolean ``` `NullReferenceException: Thrown if the atom or host provided is null.` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| obj | The IndirectObject to be assigned to this Element. | 
| host | An IndirectObject closely associated with this Atom - ideally the one that contains it. | 
| atom | The Atom to be assigned to this Element. | 
| return | Whether the assignment was made successfully. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Assign an IndirectObject to this Element. The process of assignment allows an existing IndirectObject to be viewed through the lens of a particular type of Element. It is important to ensure that IndirectObjects are assigned to appropriate types of Element. For example, while is is possible to assign a Page Indirect Object to an Image Element, such an assignment is not going to produce any useful view of the data. In addition, some assignments cannot be made at all. This occurs if if the underlying atom types are inconsistent. For example a ColorSpaceElement is based around an ArrayAtom, so attempting to assign an IndirectObject which contains a DictAtom will result in failure. Classes that inherit from this one may wish to override this function to ensure that the Atom type that is provided is acceptable. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>