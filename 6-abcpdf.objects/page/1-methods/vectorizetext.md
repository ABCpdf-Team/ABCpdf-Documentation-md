---
title: "vectorizetext"
css: "abcpdf-docs.css"
---

|  |  | VectorizeText Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Replaces the text on the page with glyph outlines. |  |  | 

</TD>
				</TR>
				<TR>
					<TD class="sectheader" vAlign="top">![](../../../images/steel-pin.gif)  

						Syntax</TD>
					<TD width="14">&nbsp;</TD>
					<TD vAlign="top">
						
| **[C#]** ```csharp void VectorizeText() ``` [Visual Basic]`Sub VectorizeText()` `may throw Exception()` |  |  | 
| --- | --- | --- |

</TD>
				</TR>
				<TR>
					<TD class="sectheader" vAlign="top">![](../../../images/steel-pin.gif)  

						Params</TD>
					<TD width="14">&nbsp;</TD>
					<TD vAlign="top">
						
| Name | Description | 
| --- | --- |
| none |  | 

</TD>
									<TD width="60">&nbsp;</TD>
									<TD width="11">&nbsp;</TD>
								</TR>
							</TBODY></TABLE>
					</TD>
				</TR>
				<TR>
					<TD class="sectheader" vAlign="top">![](../../../images/steel-pin.gif)  

						Notes</TD>
					<TD width="14">&nbsp;</TD>
					<TD vAlign="top">
						
| Use this method to vectorize the text (i.e. replace the text with equivalent glyph polygon outlines). Note that pages may sometimes share content with other pages. If this is the case then vectorizing the text on one page will also vectorize it on other pages which use this shared content. |  |  | 
| --- | --- | --- |

</TD>
				</TR>
				<TR>
					<TD class="sectheader" vAlign="top">![](../../../images/steel-pin.gif)  
Example</TD>
					<TD width="14">&nbsp;</TD>
					<TD vAlign="top">
						
| [C#] ```csharp using var doc = new Doc(); doc.FontSize = 96; doc.AddText("Hello World"); foreach (var page in doc.ObjectSoup.Catalog.Pages.GetPageArrayAll()) page.VectorizeText(); doc.Save(Server.MapPath("VectorizedText.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.FontSize = 96 doc.AddText("Hello World") For Each page As Page In doc.ObjectSoup.Catalog.Pages.GetPageArrayAll() page.VectorizeText() Next doc.Save(Server.MapPath("VectorizedText.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</TD>
				</TR>
			</TBODY></TABLE>