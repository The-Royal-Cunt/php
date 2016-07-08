The PagSeguro library in PHP is a set of domain classes that make it easier for the PHP developer, the use of features that PagSeguro offers in the form of APIs With the installed and configured the library, you can easily integrate features like.:

Create payment requests
Create signature requests
Cancel subscriptions
consult signatures
Consult code for transactions
Consult transactions by date range
Consult abandoned transactions
receive notifications
requirements

PHP 5.4.27+
SPL
cURL
SUN
Installation

Download the repository as a zip file or make a clone;
Unzip the files on your computer;
Within the source directory are two directories: the examples and PagSeguroLibrary. The examples directory contains examples of using the API calls and PagSeguroLibrary directory contains the actual library. If you want to import only the library, upload PagSeguroLibrary directory and add the PagSeguroLibrary.php class in your project. This class will be responsible for importing all library features on your system.
Installation via Composer

Alternatively, you can use Composer to load the library (PagSeguro / php).
{
    "Require": {
       "PagSeguro / php", "@stable"
    }
}
Configuration

To make real use of the library, you must make some settings in 'PagSeguroConfig.php' file, which is in the 'config' directory. The available options are described below.

environment: accept the values ​​production and sandbox. To use the sandbox, you must create an account in https://sandbox.pagseguro.uol.com.br.
email: e-mail registered in PagSeguro.
token production: token generated in PagSeguro.
token sandbox: token generated in the Sandbox.
appId production: application generated in PagSeguro.
appId sandbox: application generated in the Sandbox.
AppKey production: application token in PagSeguro.
AppKey sandbox: application token in the Sandbox.
charset: codification of your system (ISO-8859-1 or UTF-8).
log: enable / disable the generation of logs.
FileLocation: where you want to create the log file. Ex .: /logs/ps.log.
More information is available in the official documentation.

Doubts?

If you have questions or need support, please visit our forum.

changelog

2.7.1

Possibility to define installments without interest.
Adjustments in general.
2.7.0

Integration Subscription consultation service (preapproval) notification code.
2.6.0

Env Variables for integration with Laravel 5 # 0a2c2ba
Wrapper for the configuration file # c1b0985
API implementation signatures # 7cd8147
Integration with cancellation request service.
Adjustments in general.
Obs .: Some of the features described are not yet commercially available for all sellers. For questions visit our forum.
2.5.0

Ability to set discounts through payment during the checkout code request - See example createPaymentRequest.php
2.4.0

Integration with transactions consultation service / permits by reference code.
Integration with application service model.
Integration with chargeback request service.
Adjustments in general.
Obs .: The features described above are not yet commercially available for all sellers. For questions visit our forum.
2.3.0

Added classes and methods for using Checkout Transparent.
Consultations notification code and transaction code start using the new version of the APIs.
2.2.4

Added setEnvironment method in class PagSeguroConfig
Improvements in the documentation / code comments
various adjustments
2.2.3

Adjustments in the code
2.2.2

Adding sandbox environment
2.2.1

Set in the XML returned in treatment requests made to PagSeguro
2.2.0

By registering the transaction it is possible to obtain only the checkout code for use in a lightbox checkout (see example createPaymentRequestLightbox.php). Obs .: This feature is not yet commercially available for all sellers.
2.1.9

"Aesthetic" improvements in the code, such as indenting / formatting.
2.1.8

Update of means of payment codes.
Improved identification of minimum requirements for operation.
Improvement in the treatment of related address data.
2.1.7

Added: Classes for handling metadata and generic parameters.
2.1.6

Added: Class for handling sender documents, ex. CPF.
2.1.5

Added: url submission functionality notification via checkout request.
Added: New features for data processing in the helper.
Correction: Treatment double space sender name of the checkout request.
2.1.4

Added: Class for handling coins allowed in transactions with PagSeguro.
2.1.3

Correction: The request was aborted if the log generation was active and the user did not have to file log generation or writable and read to the file.
2.0.0 - 2.1.2

Classes domains representing payments, notifications and transactions.
checkouts creation via API.
Controller to process payment notifications sent by PagSeguro.
transaction query module.
License

Copyright 2013 PagSeguro Internet LTDA.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may Obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, distributed under the License is distributed on an software "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

Grades

The PagSeguro only accepts payment using the Brazilian Real (BRL).
Make sure the email and informed token are related to an account that has the vendor or business profile.
Make sure you have correctly set the charset according to the encoding (ISO-8859-1 or UTF-8) from your system. This will prevent the transactions generate possible errors or failures or even special characters may be displayed differently from the usual way.
For normally occurs generating logs, make sure that the directory and the log file has read and write permissions.
To use the transparent checkout, the activation request is required along with PagSeguro team, more information can be found at Receiving payments by PagSeguro.
Doubts?

For questions visit our forum.

Contributions

He found and fixed a bug or have a feature in mind and want to contribute?

Take a fork
Add feature or bug fix (git checkout -b my-new-feature)
Commit your changes (git commit -am 'Added some feature')
Turn a push to the branch (git push origin my-new-feature)
Please Pull Request
Obs .: Add examples for your new feature. If your Pull Request is related to a specific version, the Pull Request should not be sent to the master branch but to the corresponding branch version.

