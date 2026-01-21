---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | ObjectSoupSubset Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A set of IndirectObjects from an ObjectSoup. This may be used for selecting related objects and copying them to a new soup while maintaining the relationships between the items in the selection. ``` System.Object WebSupergoo.ABCpdf13.Objects.ObjectSoupSubset ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| ObjectSoupSubset | Construct an ObjectSoupSubset. | 
| CopyTo | Copy the objects in this subset to a new soup while preserving the relationships between the items in the selection. | 
| AddFamily | Add a parent object along with all objects it refers to. | 
| AddOnlyOne | Add just this object ignoring any objects it may refer to. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Property | Description | 
| --- | --- |
| Objects | The collection of IndirectObjects currently contained in the subset. | 
| RemapIDs | Gets the dictionary used to map object IDs from the source soup to new object IDs in the final soup. | 
| RemapTypes | A dictionary used to redirect all objects of a specific type to a specific object ID. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
        <tr> 
          <td>&nbsp; </td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
</table>