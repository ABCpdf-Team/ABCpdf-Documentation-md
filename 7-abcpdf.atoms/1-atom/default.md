---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | Atom Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A PDF atomic object comprising a basic chunk of PDF data. If you are going to be using Atoms then you will want to download the Adobe PDF Specification. This document explains the names and types that can be used and how they are interpreted. Common Operations. Get a named property from the dictionary of an IndirectObject. In the example below we use the Type property which is typically a name but the principles are similar for other entries of other types: [C#] ```csharp NameAtom type = io.Resolve(Atom.GetItem(io.Atom, "Type")) as NameAtom; ``` [Visual Basic] ```vbnet Dim type As NameAtom = io.Resolve(Atom.GetItem(io.Atom, "Type")) ``` Get an value out of an array atom. In the the event that the atom is not an array or does not have sufficient entries then the return value will be null. In the example below we are looking for entry two - this is the third entry since entries are zero based: [C#] ```csharp NumAtom num = io.Resolve(Atom.GetItem(atom, 2)) as NumAtom; ``` [Visual Basic] ```vbnet Dim num As NumAtom = io.Resolve(Atom.GetItem(atom, 2)) ``` Get a stream referenced from a property of an IndirectObject. In the example below we use the FontFile2 property (a reference to an embedded TrueType font): [C#] ```csharp StreamObject stream = io.ResolveObj(Atom.GetItem(io.Atom, "FontFile2")) as StreamObject; ``` [Visual Basic] ```vbnet Dim stream As StreamObject = io.ResolveObj(Atom.GetItem(io.Atom, "FontFile2")) ``` Add a named entry to an IndirectObject. In the example below we add a V entry which is a string. We keep the returned StringAtom so we can manipulate the value: [C#] ```csharp StringAtom str = (StringAtom)Atom.SetItem(io.Atom, "V", new StringAtom()); ``` [Visual Basic] ```vbnet Dim str As StringAtom = Atom.SetItem(io.Atom, "V", New StringAtom()) ``` Add a named entry to an IndirectObject. In the example below we add an array entry to specify a border array. Rather than creating an ArrayAtom and specifying the individual values we just specify the raw string value of the object: [C#] ```csharp Atom.SetItem(io.Atom, "Border", Atom.FromString("[ 0 0 1 ]")); ``` [Visual Basic] ```vbnet Atom.SetItem(io.Atom, "Border", Atom.FromString("[ 0 0 1 ]")) ``` | 

``` System.Object WebSupergoo.ABCpdf13.Atoms.Atom WebSupergoo.ABCpdf13.Atoms.ArrayAtom WebSupergoo.ABCpdf13.Atoms.BoolAtom WebSupergoo.ABCpdf13.Atoms.DictAtom WebSupergoo.ABCpdf13.Atoms.NameAtom WebSupergoo.ABCpdf13.Atoms.NullAtom WebSupergoo.ABCpdf13.Atoms.NumAtom WebSupergoo.ABCpdf13.Atoms.RefAtom WebSupergoo.ABCpdf13.Atoms.OpAtom WebSupergoo.ABCpdf13.Atoms.StringAtom Implements: ICloneable, IDisposable, IEquatable, IComparable ```

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| S» FromString | Create an appropriate type of Atom from a raw PDF string representation. | 
| S» GetBool | Gets the Boolean value from the Atom if it is a BoolAtom. | 
| S» GetDouble | Gets the double value from the Atom if it is a NumAtom. | 
| S» GetID | Gets the Object ID value from the Atom if it is a RefAtom. | 
| S» GetInt | Gets the integer value from the Atom if it is a NumAtom. | 
| S» GetItem | Gets the specified item from the Atom if it is of a type which contains other Atoms. | 
| S» GetName | Gets the Name value from the Atom if it is a NameAtom. | 
| S» GetText | Gets the Text value from the Atom if it is a StringAtom. | 
| S» RemoveItem | Removes the named entry from the Atom if it is a DictAtom. | 
| S» SetItem | Adds a specified item to the Atom if it is of a type which contains other Atoms. | 
| GetData | The byte array representation of the Atom as it would appear in a PDF. | 
| Clone | Creates a deep copy of the current Atom. | 
| Dispose | Dispose of the object. | 
| Equals | Test whether the two Atoms are the same. | 
| GetHashCode | A hash code for the Atom. | 
| ToString | The string representation of the Atom as it would appear in a PDF. | 

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
| none |  | 

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