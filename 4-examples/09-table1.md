# Small Table Example

## Setup

We start by creating our document object and reading the data for our table. For the purposes of this example we'll assume that our data is in a standard tab delimited format.

[C#] string text = File.ReadAllText(Server.MapPath("text6.txt")); using var doc = new Doc(); // set up document doc.FontSize = 16; doc.Rect.Inset(20, 20); [Visual Basic] Dim theText As String = File.ReadAllText(Server.MapPath("text6.txt")) Using doc As New Doc() ' set up document doc.FontSize = 16 doc.Rect.Inset(20, 20)

## Rotate

We create a new table object passing in values to tell it what rectangle it can occupy (it takes the current document rectangle) and how many columns of data it should be prepared for.

Columns are assigned relative widths and expand horizontally to fit the table rectangle. Here we're specifying five columns.

Most of our columns will be right aligned so we set the default horizontal alignment to 1.

[C#] var table = new PDFTable(doc, 5); table.CellPadding = 5; table.HorizontalAlignment = 1; [Visual Basic] Dim theTable As New PDFTable(doc, 5) theTable.CellPadding = 5 theTable.HorizontalAlignment = 1

## Add

We iterate through the table data adding rows as we go. We override the right alignment for the first column and we shade alternating rows using a light gray color. Finally we frame the table and save the document.

[C#] text = text.Trim(); text = text.Replace("\r\n", "\r"); string[] theRows = text.Split(new char[] { '\r' }); for (int i = 0; i < theRows.Length; i++) { table.NextRow(); string[] theCols = theRows[i].Split(new char[] { '\t' }); theCols[0] = "<stylerun hpos=0>" + theCols[0] + "</stylerun>"; table.AddTextStyled(theCols); if ((i % 2) == 1) table.FillRow("220 220 220", i); } table.Frame(); doc.Flatten(); doc.Save(Server.MapPath("table1.pdf")); [Visual Basic] theText = theText.Trim() theText = theText.Replace(vbCr & vbLf, vbCr) Dim theRows As String() = theText.Split(New Char() {ControlChars.Cr}) Dim i As Integer = 0 While i < theRows.Length theTable.NextRow() Dim theCols As String() = theRows(i).Split(New Char() {ControlChars.Tab}) theCols(0) = "<stylerun hpos=0>" + theCols(0) + "</stylerun>" theTable.AddTextStyled(theCols) If (i Mod 2) = 1 Then theTable.FillRow("220 220 220", i) End If System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While theTable.Frame() doc.Flatten() doc.Save(Server.MapPath("table1.pdf")) End Using

## Results

Using the following input data:

Planet Distance From Sun (miles) Diameter (miles) Year Length (days) Day Length (days) Mercury 36,000,000 3,030 88 58.00 Venus 67,000,000 7,520 225 225.00 Earth 93,000,000 7,925 365 1.00 Mars 142,000,000 4,210 687 1.00 Jupiter 484,000,000 88,730 4,344 0.40 Saturn 888,000,000 74,975 10,768 0.40 Uranus 1,800,000,000 31,760 30,660 0.70 Neptune 2,800,000,000 30,600 60,150 0.65 Pluto 3,600,000,000 1,410 90,520 0.25

We get the following output.

table1.pdf

