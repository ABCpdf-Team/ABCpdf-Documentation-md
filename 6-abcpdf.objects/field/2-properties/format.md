# Format Property

## Notes

The format for this field.

The PDF specification does not define how fields should be formatted. Acrobat uses a set of standard JavaScripts to perform field formatting.

This property reflects the JavaScript formatting function which is being used and the values which are being passed to it. A typical value might be:

AFNumber_Format(2, 3, 0, 0, "", true);

This defines a number format with two decimal places. Other typical formatting functions you will see include AFPercent_Format, AFSpecial_Format, AFDate_Format and AFTime_Format.

For a definitive guide to these formatting functions you should see the JavaScripts which come installed with your version of Acrobat. However as of early 2019, the following are defined.

AFNumber_Format(decimals, separator, negative, unused, currency, prepend); AFPercent_Format(decimals, separator); AFSpecial_Format(special_type) AFDate_Format(date_type) AFDate_FormatEx(date_time_format) AFTime_Format(time_type) AFTime_FormatEx(date_time_format)

The number of figures to display after the decimal point.

eg for "2" the output might be "1,234.567".

A number indicating the style of separators for thousands and decimal points.

A number indicating the style for negative numbers.

This parameter is currently unused.

A string indicating the currency symbol to be added to numbers.

eg for "$" the output might be "$1,234.56".

A boolean which; if true, indicates that the currency symbol should be prepended; and if false, that it should be appended.

eg for "false" the output might be "1,234.56 €".

A number indicating a fixed format style used for structures such as telephone numbers and zip codes.

A number indicating a format style used to indicate a date.

See date_time_format below for details of the format.

A number indicating a format style used to indicate a time.

See date_time_format below for details of the format.

A string indicating style used to format a date or time.

See date_type above for examples of the types of styles you can use.

The "m" and "mm" sequences indicate the month using a one and two digit number respectively - the former being of limited use. The "mmm" and "mmmm" sequence indicates the month using a short three character and full name respectively.

The "d" and "dd" sequences indicates the ordinal day of the month (the former being of limited use) while the "ddd" and "dddd" sequences indicate the day of the week using a short three character and full name respectively.

The "yy" indicates the short form of the year and the "yyyy" selector indicates the long form of the year.

The "h", "hh", "H" and "HH" sequences indicate the hours. The upper case versions work on the twenty-four hour clock and the lower case ones on the twelve hour clock. The one character selectors indicate the hour using one character (obviously of limited use) and the two character selectors indicate it using two characters.

The "MM" selector indicates the number of minutes past the current hour.

The "s" and "ss" selectors indicate the number of seconds past the current minute. The former uses one digit - of limited use - and the latter uses two.

The "t" and "tt" indicate the time relative to the meridiem - am or pm - using one digit or two characters respectively.

## Example

None.

