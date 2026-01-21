# XpsImportOperation Class

An operation used to import XPS and OXPS documents.

``` System.Object WebSupergoo.ABCpdf13.Operations.Operation WebSupergoo.ABCpdf13.Operations.XpsImportOperation ```

## Method Description S&raquo;&nbsp; GetApplicationFolder Gets the installation folder of an import application. XpsImportOperation XpsImportOperation Constructor. ApplicationIsRunning Gets a value indicating whether an import application is running for this XpsImportOperation. EnableApplicationReuse Enables an import application process to be reused so that it is terminated only manually or when this operation is disposed of. &nbsp;Import Imports a portion of an XPS document. ImportAny Imports a portion of a document via an intermediate XPS print-out. KillApplication Terminates a running import application. ReusesApplication Gets a value indicating whether an import application process is to be kept running and reused. &nbsp;

## Property Description AddAnnotations The types of annotations to be added. BoldWidth The percentage of boldness to apply when creating a synthetic bold style. Application The application used by ImportAny. ApplicationFolder The folder of the application used by ImportAny. DocNumber The one-based document number used by ImportAny. EnableMSOfficeMacros Whether to enable macros when opening MS Office documents. Password The password needed to read the source.