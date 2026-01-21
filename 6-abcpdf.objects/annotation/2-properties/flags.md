---
title: "flags"
css: "abcpdf-docs.css"
---

|  |  | Flags Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp AnnotationFlags ``` [Visual Basic] `AnnotationFlags` | n/a | No | The Annotation Flags entry | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property is used to access or change the flags for the annotation. The AnnotationFlags type is a flags type enumeration so the different values can be combined together using bitwise operations. It may take the following values: Invisible (Do not display the annotation if it does not belong to one of the standard types and no special handler is available) Hidden (Do not display or print the annotation or allow it to interact with the user, regardless of its type or whether an annotation handler is available) Print (Print the annotation when the page is printed. Typically used to hide pushbuttons when a page is printed) NoZoom (Do not scale the annotation as the zoom level of the page is changed. The top left of the annotation on the page remains fixed regardless of the page zoom level) NoRotate (Do not rotate the annotation as the page is rotated. The top left of the annotation on the page remains fixed regardless of the page rotation) NoView (Do not show the annotation on the screen or allow it to interact with the user. The annotation may be printed if the Print flag is set) ReadOnly (Do not allow the annotation to interact with the user) Locked (Do not allow the annotation to be moved, deleted or otherwise modified. However the content may be changed even if this property is set) ToggleNoView (Invert the interpretation of the NoView flag for certain events) LockedContents (Do not allow the contents of the annotation to be modified. Other annotation properties such as size and location may be modified) For code showing how to check, set or clear flags see the FontObject.Flags property. |  |  | 
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