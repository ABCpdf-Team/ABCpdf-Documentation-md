---
title: "02-ref"
css: "abcpdf-docs.css"
---

|  |  | Ref Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp RefAtom ``` [Visual Basic] `RefAtom` | null | Yes | Gets any RefAtom that is part of this Element. | 

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
      
| Gets any RefAtom that is part of this Element. When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom. If this is the case then the reference needs to be resolved through to an Atom. This property stores the original RefAtom and the Atom property stores the resolved Atom - usually a DictAtom. If the provided Atom is not a RefAtom then this property will be null. |  |  | 
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