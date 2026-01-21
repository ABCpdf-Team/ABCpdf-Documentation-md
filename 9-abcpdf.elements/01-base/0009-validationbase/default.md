# ValidationBase Class

ValidationBase class.

This is a class derived from Validation that stores and reports the validation status of Elements that are being validated.

It implements a variety of useful features like the detection and resolution of recursive loops, a stack trace and a coverage option.

For custom validation reports you will generally want to derive from this class and implement any abstract methods.

``` System.Object WebSupergoo.ABCpdf13.Elements.Validation WebSupergoo.ABCpdf13.Elements.ValidationBase ```

## Method Description ValidationBase Initializes a new instance of the ValidationBase class. GetStackTrace Gets the stack trace. inherited methods... &nbsp;

## Property Description HashSet&lt;string&gt; Gets all types that may be recorded in the Coverage. Coverage Gets or sets the coverage. Stack Gets or sets the stack. Done Gets the set of IDs which have been processed. inherited properties...