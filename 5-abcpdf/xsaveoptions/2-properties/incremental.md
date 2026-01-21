---
title: "incremental"
css: "abcpdf-docs.css"
---

|  |  | Incremental Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to use incremental update to preserve an audit trail. | 

</td><td width="60">&nbsp;</td><td>&nbsp;</td></tr> 
</table></td></tr> <tr> <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td><td width="14">&nbsp;</td><td valign="top"> 

| This property determines if incremental update should be used.Incremental update leaves the structure of any original document intact and appends any changes to the end of the file. Because the original PDF is unchanged it is possible to revert back to the state before the changes were applied. Because only updated objects are written to disk it can result in faster write times.However most importantly you have to use incremental update if you wish to preserve any signed signature fields present in the document. Indeed after any signature field is signed you need to commit changes to file using incremental update. Incremental Update is incompatible with the Linearization, Remapping and CompressObjects options. As such it will override these settings. If you are incrementally updating an encrypted document the encryption settings must remain identical between incremental updates. For this reason it is important to read the document in a particular way. Only one password is required to Doc.Read an encrypted document but to save it two passwords are required. For this reason it is important to read the document using the user password (typically blank) and then set both the Doc.Encryption.Password and the Doc.Encryption.OwnerPassword before doing an incremental save. You need to know both passwords in order to update the document. |  |  | 
| --- | --- | --- |

</td></tr> <tr> <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td><td width="14">&nbsp;</td><td valign="top"> 

| None. |  |  | 
| --- | --- | --- |

</td></tr> </table>