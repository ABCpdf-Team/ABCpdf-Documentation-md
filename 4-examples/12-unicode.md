# Unicode Example

## Setup

First we create an ABCpdf Doc object and set the font size.

[C#] using var doc = new Doc(); doc.FontSize = 32;

## Read

We read in our Japanese text from a Unicode text file.

[C#] string path = "../Rez/Japanese2.txt"; string text = File.ReadAllText(path);

## Add

Because we want to ensure that our document renders correctly on all platforms we're going to embed our font in Unicode format. We specify a left-to-right writing direction and we choose to subset our font.

Please note when embedding fonts you must ensure you have permission to embed and redistribute the embedded font as part of your PDF.

[C#] doc.Page = doc.AddPage(); doc.Font = doc.EmbedFont("MS PGothic", LanguageType.Unicode, false, true); doc.AddText("Japanese" + text);

## Add

Just to show how it works we'll also render a page in vertical writing mode.

[C#] doc.Page = doc.AddPage(); doc.Font = doc.EmbedFont("MS PGothic", LanguageType.Unicode, true, true); doc.AddText("Japanese" + text);

## Save

Finally we save at a specified location.

[C#] doc.Save("unicode.pdf"); // finished

## Results

We get the following output.

