---
title: "makefieldnamesunique"
css: "abcpdf-docs.css"
---

|  |  | MakeFieldNamesUnique Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether field names should be changed to make them unique. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </tbody></table>
    </td>
  </tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| HTML forms can contain fields with the same name. If the names of two fields in a PDF are the same, then the fields take the same value. So if multiple HTML fields with the same name are added to a PDF, these fields will all appear to contain the same content. This is true even if the original HTML fields contained different content. Setting this property will result in duplicate fields being renamed to allow the content to be different. The ABCChrome engine does not support this property but it is not a difficult matter to emulate it using code of the following form. [C#] ```csharp HashSet names = new HashSet(); List fields = new List(); foreach (Field field in theDoc.Form.Fields) { fields.Add(field); foreach (Field kid in field.GetKids(1000)) fields.Add(kid); } foreach (Field field in fields) { for (int i = 1; names.Contains(field.Name); i++) Atom.SetItem(field.Atom, "T", new StringAtom(field.PartialName + "_" + i.ToString())); names.Add(field.Name); } theDoc.Form.Refresh(); ``` [Visual Basic] ```vbnet Dim names As HashSet(Of String) = New HashSet(Of String) Dim fields As List(Of Field) = New List(Of Field) For Each field As Field In theDoc.Form.Fields fields.Add(field) For Each kid As Field In field.GetKids(1000) fields.Add(kid) Next Next For Each field As Field In fields Dim i As Integer = 1 Do While names.Contains(field.Name) Atom.SetItem(field.Atom, "T", New StringAtom((field.PartialName + ("_" + i.ToString)))) i = (i + 1) Loop names.Add(field.Name) Next theDoc.Form.Refresh ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</tbody></table>