---
title: "metadata"
css: "abcpdf-docs.css"
---

|  |  | Metadata Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp Metadata ``` [Visual Basic] `Metadata` | n/a | No | Any document level Metadata. | 

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
      
| Any document level Metadata. The Metadata object holds XMP metadata such as Title, Author, Subject, Keywords, Creator, Creation Date and Modification Date. There are multiple places that document level metadata can be stored in a PDF. The most commonly used are the Info entry of the Trailer and the Metadata entry of the Catalog. The Info entry is the older and most widely recognized location. The Metadata entry is a more recent XML based store introduced in PDF 1.4. It is important that information within these stores is consistent. If the information is inconsistent then you will find that the metadata reported by different applications is different. To try and reduce the amount of confusion caused by multiple metadata entries, PDF 2.0 deprecated all Info entries apart from the CreationDate and ModDate. To be PDF 2.0 compliant you should put all metadata into the Metadata entry rather than the Info one. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This example shows how to insert document properties. Document properties can be viewed from Acrobat Reader and most commonly provide information on the document origin. Complex XMP metadata can be constructed using the Adobe XMP Toolkit. However in most cases you will only want simple metadata so you can use the use the standard Metadata object properties. Here we load an existing PDF and set the Title and Author. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../mypics/book.pdf")); var md = doc.ObjectSoup.Catalog.Metadata; if (md == null) { md = new Metadata(doc.ObjectSoup); doc.ObjectSoup.Catalog.Metadata = md; } md.InfoSubject = "Finn Family Moomintroll"; md.InfoAuthor = "Tove Jansson"; doc.Save(Server.MapPath("metadata.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../mypics/book.pdf")) Dim md As Metadata = doc.ObjectSoup.Catalog.Metadata If md = Nothing Then md = New Metadata(doc.ObjectSoup) doc.ObjectSoup.Catalog.Metadata = md End If md.InfoSubject = "Finn Family Moomintroll" md.InfoAuthor = "Tove Jansson" doc.Save(Server.MapPath("metadata.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>