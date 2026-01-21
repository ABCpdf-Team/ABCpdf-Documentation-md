---
title: "01-autodetectfactory"
css: "abcpdf-docs.css"
---

|  |  | AutodetectFactory Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Autodetect Factory. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static Element AutodetectFactory(Atom atom, IndirectObject host, object reference) ``` [Visual Basic] ``` Shared Function AutodetectFactory(atom As Atom, host As IndirectObject, reference As object) As Element ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| atom | The atom from which the Element should be created. | 
| host | The host object. This can be any IndirectObject in the document but it is useful to specify one with which the atom is closely associated. | 
| reference | A reference which may be used to pass context. | 
| return | An Element or Element subclass. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Autodetect Factory. This is used for the creation of specific types of Element based on the content of the Atom. Many Atoms have specific Type or Subtype fields which are used to indicate the precise variant of Element. If these are present, which in many cases they are, then a sensible choice can be made as to the type of Element to create. Even when these are not present sometimes it is possible to detect the type from specific combinations of entries found in the Atom. However not all specializations can be auto-detected as not all require this type of identification element. If this is the case then the return value will be a generic Element. |  |  | 
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