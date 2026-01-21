---
title: "getresourcesbytype"
css: "abcpdf-docs.css"
---

|  |  | GetResourcesByType Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Get all the resources of a named type, optionally including any used by referenced objects. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp ISetAtom> GetResourcesByType(string type, bool annotations, bool patterns, bool xobjects, bool parents, ISet skip) ``` [Visual Basic] ``` Function GetResourcesByType(type As String, annotations As Boolean, patterns As Boolean, xobjects As Boolean, parents As Boolean, skip As ISet(Of Integer)) As ISet(Of Atom) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| type | The type of resource to be found. | 
| annotations | Whether to include resources in annotations. | 
| patterns | Whether to include resources in pattern dictionaries. | 
| xobjects | Whether to include resources in referenced Form XObjects. | 
| parents | Whether to include resources in parent objects. | 
| skip | A set of IndirectObject IDs that should be skipped when performing the scan. May be null. | 
| return | A set of matching resource Atoms. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Get all the resources of a named type, optionally including any used by referenced objects. This can, for example, be used to find all the FontObjects referenced in the "Font" section of the page. Optionally you can include annotations, patterns, Form XObjects and parent objects in the scan and generally this is something you will want to do. If you are performing multiple operations of this type you may wish to include a set of IndirectObject IDs that should be skipped. On return the set will have been updated and all the new IndirectObjects that have been scanned will have been added. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>