---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | Field Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Represents a field in a document. The PDF specification makes a distinction between a field (in terms of a named value) and the visible appearance of the field on the document. So not every field has a visible appearance. Those that do can be located using the Page and Rect properties. The value of the field can be modified using the Value property. Fields exist within a hierarchy. Fields have children and their children can have children in turn. You can drill down through the hierarchy using the Kids property. Alternatively - given a fully qualified name - you can use the XForm level methods to obtain references directly. Note that the Field object is an abstraction of the underlying objects defined in the document. As such the Object ID may refer to an Annotation Widget or it may refer to a Field or it may refer to a hybrid Widget Field as defined in the PDF specification. ``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.Field ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| Focus | Prepare document for drawing at the field location. | 
| GetAnnotations | Gets all the Annotations referenced by this field or its children. | 
| GetKids | Gets a set of Fields that are descendents of this one. | 
| GetExportValues | Gets the export values for this field. | 
| SetFont | Sets the font and font size to be used for text. | 
| Stamp | Stamp this field into the document. | 
| UpdateAppearance | Update the appearance of all the Annotations associated with this field. | 
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
| DefaultAppearance | The default appearance (DA) used for the text. | 
| FieldType | The field type. | 
| Flags | The Field Flags (Ff) entry. | 
| Format | The field format. | 
| Kids | All the immediate children of this field. | 
| MultiSelect | Whether the field supports multiple selections. | 
| Name | The fully qualified field name. | 
| Options | The field options. | 
| Page | The Page on which the field appears. | 
| PageID | The ID of the page on which the field appears. | 
| Parent | The parent of this field. | 
| PartialName | The partial field name. | 
| Rect | The location and size of the field. | 
| TextAlignment | The alignment for the text. | 
| TextColor | The color used for the text. | 
| TextFont | The font used for the text. | 
| TextSize | The font size used for the text. | 
| Value | The field value. | 
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