---
title: "10-table2"
css: "abcpdf-docs.css"
---

|  |  | Large Table Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This example shows how to draw a multi-page table. ABCpdf does not provide table drawing routines itself so this example uses a Table Class to position the table elements. You can find the full project and classes under the ABCpdf menu item. The project includes code for laying out a small table, a large table spreading over more than one page, an invoice and a product list. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Setup</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We start by creating our document object and reading the data for our table. For the purposes of this example we'll assume that our data is in a standard tab delimited format. [C#] ```csharp string text = File.ReadAllText(Server.MapPath("text7.txt")); using var doc = new Doc(); // set up document doc.FontSize = 12; doc.Rect.Inset(20, 20); ``` [Visual Basic] ```vbnet Dim theText As String = File.ReadAllText(Server.MapPath("text7.txt")) Using doc As New Doc() ' set up document doc.FontSize = 12 doc.Rect.Inset(20, 20) ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Rotate</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We create a new table object passing in values to tell it what rectangle it can occupy (it takes the current document rectangle) and how many columns of data it should be prepared for. Columns are assigned relative widths and expand horizontally to fit the table rectangle. Here we're specifying six columns and a number of relative widths. We're padding the cells so there are gaps between the rows and columns. Finally we specify a header which repeats as new pages are added. [C#] ```csharp PDFTable theTable = new PDFTable(doc, 6); // some columns extra width theTable.SetColumnWidths(new double[] { 2, 1, 3, 2, 1, 4 }); theTable.CellPadding = 5; theTable.RepeatHeader = true; ``` [Visual Basic] ```vbnet Dim theTable As New PDFTable(doc, 6) ' some columns extra width theTable.SetColumnWidths(New Double() {2, 1, 3, 2, 1, 4}) theTable.CellPadding = 5 theTable.RepeatHeader = True ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Add</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| We iterate through the table data adding rows and columns as we go. Every time we add a row we check to see if the page number has changed and restart the shading if it has. This ensures the header is always unshaded. Finally we save the document. [C#] ```csharp text = text.Replace("\r\n", "\r"); string[] theRows = text.Split(new char[] { '\r' }); int thePage = 1; bool theShade = false; for (int i = 0; i thePage) { thePage = doc.PageNumber; theShade = true; } if (theShade) theTable.FillRow("200 200 200", theTable.Row); theShade = !theShade; } doc.Flatten(); doc.Save(Server.MapPath("table2.pdf")); ``` [Visual Basic] ```vbnet theText = theText.Replace(vbCr & vbLf, vbCr) Dim theRows As String() = theText.Split(New Char() {ControlChars.Cr}) Dim thePage As Integer = 1 Dim theShade As Boolean = False Dim i As Integer = 0 While i thePage Then thePage = doc.PageNumber theShade = True End If If theShade Then theTable.FillRow("200 200 200", theTable.Row) End If theShade = Not theShade System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While doc.Flatten() doc.Save(Server.MapPath("table2.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../images/steel-pin.gif)  
Results</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Using a large quantity of input data. We get the following output. table2.pdf - [Page 1] table2.pdf - [Page 2] | table2.pdf - [Page 3] | 
| --- | --- |
| table2.pdf - [Page 4] | table2.pdf - [Page 5] | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
</table>