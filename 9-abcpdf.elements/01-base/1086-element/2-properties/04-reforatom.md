---
title: "04-reforatom"
css: "abcpdf-docs.css"
---

|  |  | RefOrAtom Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Atom ``` [Visual Basic] `Atom` | null | Yes | Gets the Atom that was used to create this Element. | 

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
      
| Gets the Atom that was used to create this Element. When an Atom is provided during construction, this may be a reference to an IndirectObject rather than a direct reference to an Atom. If this is the case then the reference needs to be resolved through to an Atom. The Ref property stores the RefAtom, if one was provided. The Atom property stores the resolved Atom. This property will return the Ref if it is not null, or the Atom if it is. |  |  | 
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