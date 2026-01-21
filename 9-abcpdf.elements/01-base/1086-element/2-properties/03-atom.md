---
title: "03-atom"
css: "abcpdf-docs.css"
---

|  |  | Atom Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Atom ``` [Visual Basic] `Atom` | null | Yes | Gets any Atom that is part of this Element. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Gets any Atom that is part of this Element. When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom. If this is the case then the reference needs to be resolved through to an Atom. This property stores the resolved Atom - usually a DictAtom but occasionally other types for some specific types of Element. However this property will never be a RefAtom as all references have been resolved. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>