---
title: "03-entrylookup"
css: "abcpdf-docs.css"
---

|  |  | EntryLookup Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | This property represents the lookup table for the palette. | 

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
      
| This property represents the lookup table for the palette. The lookup may be represented as a StreamElement or (in PDF 1.2) a byte string. The table shall contain a number of colors one higher than the EntryHiVal. Each color shall contain a number of byes equal to the number of components in the EntryBaseColorSpace. Each byte represents an intensity of color from 0 to 255 - 0% to 100% respectively. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 156. |  |  | 
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