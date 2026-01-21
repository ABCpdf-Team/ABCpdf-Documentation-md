---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | ArrayAtom Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| An Atom containing an array of other Atoms. ``` System.Object WebSupergoo.ABCpdf13.Atoms.Atom WebSupergoo.ABCpdf13.Atoms.ArrayAtom Implements: IList, ICollection, IEnumerable, IList, ICollection, IEnumerable ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| S» FromXRect | Create an ArrayAtom from a XRect representation. | 
| S» FromXTransform | Create an ArrayAtom from a XTransform representation. | 
| S» FromContentStream | Create an array of Atoms from a byte array containing a sequence of PDF objects. | 
| S» FromNames | Create an ArrayAtom of NameAtoms from a list of strings. | 
| S» FromStrings | Create an ArrayAtom of StringAtoms from a list of strings. | 
| S» FromNums | Create an ArrayAtom of NumAtoms from a list of numbers. | 
| ArrayAtom | ArrayAtom Constructor. | 
| CopyTo | Copies the Atoms into an array. | 
| Add | Add an item to the end of the array. | 
| Clear | Removes all Atoms from the array. | 
| Contains | Determines whether the array contains a specific Atom. | 
| IndexOf | Determines the index of a specific Atom. | 
| Insert | Inserts an Atom into the array at the specified position. | 
| Remove | Removes an Atom from the array. | 
| RemoveAt | Removes an Atom at a specified position from the array. | 
| AddRange | Adds the elements in the supplied array at the end of this array. | 
| Equals | Test whether the two ArrayAtoms are the same. | 
| GetEnumerator | Gets an enumerator for the Collection. | 
| GetRange | Creates a shallow copy of a range of elements in the source array. | 
| InsertRange | Inserts the elements in the supplied array into this array at the specified index. | 
| RemoveRange | Removes a range of elements from the source array. | 
| ToString | The string representation of the StringAtom as it would appear in a PDF. | 
|  | inherited methods... | 

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
| Count | The number of Atoms in the array. | 
| Item | Get or set the Atom at the specified index. | 
| IsContentStream | Determines whether the ArrayAtom represents a content stream or not. | 
| ItemsPerLine | Determines the number of items that will be output per line when serializing an array. | 
|  | inherited properties... | 

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