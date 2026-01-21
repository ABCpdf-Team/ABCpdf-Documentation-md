---
title: "icccmyk"
css: "abcpdf-docs.css"
---

|  |  | IccCmyk Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "standard" | No | The path to the default CMYK ICC color profile. | 

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
      
| A path to the default CMYK ICC color profile. The profile that will be used to convert any device CMYK specified in the PDF file to the device independent working color space. This may be necessary when colors in different color spaces need to be blended together. This property can take a path to an icm file. However there are also two special values you can use. If the property takes the value "device" then the device color space will be used. If the property takes the value "standard" then a built in default color profile will be used. If this property is set to "standard" or a path to a color profile then IccRgb, IccCmyk, IccGray and IccOutput should also be set to "standard" or paths to color profiles. All color spaces are assumed to be device independent color spaces. If this property is set to "device" then IccRgb, IccCmyk, IccGray and IccOutput should also be set to "device". All color spaces are all assumed to be device color spaces. If this property is set to a file name with no path information, then the system ICC color profile directory will be searched to locate the file. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>