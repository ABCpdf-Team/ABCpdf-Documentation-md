# Upgrading

## Basics

ABCpdf 13 is a new version completely independent of the old. It incorporates the ABCpdf2, ABCpdf3, ABCpdf4, ABCpdf5, ABCpdf6, ABCpdf7, ABCpdf8, ABCpdf9, ABCpdf10, ABCpdf11 and ABCpdf12 namespaces so that you can upgrade with minimal changes to your code. When you want to take advantage of the new features, simply reference the new name.

Simply replace...

[C#] using WebSupergoo.ABCpdf12;

with...

[C#] using WebSupergoo.ABCpdf13;

## Changes

ABCpdf is fully backward compatible. Although extensive changes have been made to the core engine, we check that these changes produce results that are compatible with previous versions.

There are some minor differences in behavior between the ABCpdf12 and ABCpdf13 namespaces.

The new ABCChrome123 HTML conversion engine is our new default as it is faster, more compliant and more secure than the previous one. If your HTML conversions rely on specific output styles created by the previous default engines - eg ABCChrome86 - you will want to use the following line of code after creating any Doc object, after calling Doc.Read and after calling Doc.Clear.

[C#] doc.HtmlOptions.Engine = EngineType.Chrome86;

For this release we have vastly increased the capabilities of FireShield. It has much greater insight into what is happening in the current process and intercepts requests that previously might have gone unnoticed. This means that if you have custom rules for FireShield it may pick up some events - for example file information queries - which previously it might not have done. Your rules may need to be adjusted to allow these types of events to be ignored as appropriate.

You should not use objects after disposal. However the debugger does not know if an object is disposed so if you are displaying disposed objects in the watch window you may see exceptions being thrown. We have changed behavior here to make disposed objects more tolerant of misuse. Properties such as the XEncryption.StreamCryptionMethod and XEncryption.StringCryptionMethod are likely to return default values rather than throw exceptions.

The app.config ABCpdf preferences section has been changes slightly. In Version 12 we had an <ABCpdf12.Section> tag but in version 13 is is simply <ABCpdf13>. We handle the camel cased XML preferences for backwards compatibility but in the current release we prefer lower case entries. See the XSettings.SetConfigFile function for details.

