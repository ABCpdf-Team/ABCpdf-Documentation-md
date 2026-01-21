---
title: "getresourcemap"
css: "abcpdf-docs.css"
---

|  |  | GetResourceMap Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get a dictionary mapping the names of a particular type of resource to Atoms |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IDictionaryAtom> GetResourceMap(string type) IDictionaryAtom> GetResourceMap(string type, bool includeXObjects, bool includePatterns, ISet skip, ISetAtom> set) ``` [Visual Basic] ``` Function GetResourceMap(type As String) As IDictionary(Of string, Atom) Function GetResourceMap(type As String, includeXObjects As Boolean, includePatterns As Boolean, skip As ISet{Of Integer}, set As System.Collections.Generic.ISet{Of Atom}) As IDictionary(Of string, Atom) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| type | The type of resource to be indexed. | 
| includeXObjects | Whether to include resources from other Form XObjects referenced from this one. | 
| includePatterns | Whether to include resources from Patterns referenced from this Form XObject. | 
| skip | A set of IDs indicating IndirectObjects that should be skipped. This value may be null if you do not want to skip any items. | 
| set | A set of IDs of all the resources that have been encountered. The set of resources is generally the same as the set of items in the returned dictionary, but may not be if resource names have clashed. This value may be null if you are not interested in the set. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Get a dictionary mapping the names of a particular type of resource to Atoms. The Atoms returned are typically RefAtom objects referring to an IndirectObject. However some resource types (notably color spaces) may be referred to direct. It is unusual to look up just one resource name. Typically one has a sequence of resource names from a content stream which all need resolving. For this reason it is best to use this function to obtain a map which can then be cached. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>