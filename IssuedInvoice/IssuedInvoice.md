# IssuedInvoice

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/IssuedInvoice](https://moj.minimax.si/SI/API/Home/ModuleDetails/IssuedInvoice)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddIssuedInvoice](#addissuedinvoice) | Adds a new issued invoice. |
| 2 | 🔵 `POST` | [AddIssuedInvoiceAttachment](#addissuedinvoiceattachment) | Adds an attachment to a given issued invoice. |
| 3 | 🟡 `PUT` | [CustomActionIssuedInvoice](#customactionissuedinvoice) | Performs a custom action on issued invoice.
 Available actionName values:
 
issue
issueCancellation
generatepdf
copyto |
| 4 | 🔴 `DELETE` | [DeleteIssuedInvoice](#deleteissuedinvoice) | Deletes issued invoice. |
| 5 | 🟢 `GET` | [GetIssuedInvoice](#getissuedinvoice) | Returns an issued invoice. |
| 6 | 🟢 `GET` | [GetIssuedInvoiceAttachments](#getissuedinvoiceattachments) | Returns all attachments for a given issued invoice. |
| 7 | 🟢 `GET` | [GetIssuedInvoicePaymentMethods](#getissuedinvoicepaymentmethods) | Returns all payment methods for given organisation. |
| 8 | 🟢 `GET` | [GetIssuedInvoices](#getissuedinvoices) | Returns all issued invoices for given organization. |
| 9 | 🟢 `GET` | [GetIssuedInvoicesSyncCandidates](#getissuedinvoicessynccandidates) | Returns issued invoices for sync. |
| 10 | 🟡 `PUT` | [UpdateIssuedInvoice](#updateissuedinvoice) | Updates issued invoice. |

## Kazalo metod

- 🔵 [AddIssuedInvoice](#addissuedinvoice)
- 🔵 [AddIssuedInvoiceAttachment](#addissuedinvoiceattachment)
- 🟡 [CustomActionIssuedInvoice](#customactionissuedinvoice)
- 🔴 [DeleteIssuedInvoice](#deleteissuedinvoice)
- 🟢 [GetIssuedInvoice](#getissuedinvoice)
- 🟢 [GetIssuedInvoiceAttachments](#getissuedinvoiceattachments)
- 🟢 [GetIssuedInvoicePaymentMethods](#getissuedinvoicepaymentmethods)
- 🟢 [GetIssuedInvoices](#getissuedinvoices)
- 🟢 [GetIssuedInvoicesSyncCandidates](#getissuedinvoicessynccandidates)
- 🟡 [UpdateIssuedInvoice](#updateissuedinvoice)

---

## Podrobnosti metod

### AddIssuedInvoice

🔵 **POST** &nbsp;`api/orgs/{organisationId}/issuedinvoices`

Adds a new issued invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-issuedinvoices)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoice` | issuedInvoice id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Version` |  |
| `Content` |  |
| `StatusCode` |  |
| `ReasonPhrase` |  |
| `Headers` |  |
| `RequestMessage` |  |
| `IsSuccessStatusCode` |  |

---

### AddIssuedInvoiceAttachment

🔵 **POST** &nbsp;`api/orgs/{organisationId}/issuedinvoices/{issuedInvoiceId}/attachments`

Adds an attachment to a given issued invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-issuedinvoices-issuedInvoiceId-attachments)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoiceId` | receivedInvoiceId id |
| `attachment` | attachment |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Version` |  |
| `Content` |  |
| `StatusCode` |  |
| `ReasonPhrase` |  |
| `Headers` |  |
| `RequestMessage` |  |
| `IsSuccessStatusCode` |  |

---

### CustomActionIssuedInvoice

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/issuedinvoices/{issuedInvoiceId}/actions/{actionName}?rowVersion={rowVersion}`

Performs a custom action on issued invoice.
 Available actionName values:
 
issue
issueCancellation
generatepdf
copytocreditnote
copyToReverse
issueAndGeneratepdf
sendEInvoice


Optional parameters:
 
issueCancellationReason: May be optionally used with the issueCancellation action.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-issuedinvoices-issuedInvoiceId-actions-actionName_rowVersion)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id. |
| `issuedInvoiceId` | Issued invoice id. |
| `rowVersion` | Rows version is used for concurrency check. |
| `actionName` | Available actionName values: {"issue", "issueCancellation", "generatepdf", "copytocreditnote", "issueAndGeneratepdf", "sendEInvoice"} |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Version` |  |
| `Content` |  |
| `StatusCode` |  |
| `ReasonPhrase` |  |
| `Headers` |  |
| `RequestMessage` |  |
| `IsSuccessStatusCode` |  |

---

### DeleteIssuedInvoice

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/issuedinvoices/{issuedInvoiceId}`

Deletes issued invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-issuedinvoices-issuedInvoiceId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoiceId` | issuedInvoice id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Version` |  |
| `Content` |  |
| `StatusCode` |  |
| `ReasonPhrase` |  |
| `Headers` |  |
| `RequestMessage` |  |
| `IsSuccessStatusCode` |  |

---

### GetIssuedInvoice

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoices/{issuedInvoiceId}`

Returns an issued invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoices-issuedInvoiceId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoiceId` | issuedInvoice id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `IssuedInvoiceId` | Issued invoice id. |
| `Year` | Invoice year. Readonly. |
| `InvoiceNumber` | Invoice number. Readonly. |
| `DocumentNumbering` | class DocumentNumbering. Document numbering. |
| `Customer` | class Customer. Customer. |
| `DateIssued` | Invoice date. |
| `DateTransaction` | Date of transaction. |
| `DateTransactionFrom` | Start date of transaction. |
| `DateDue` | Invoice due date. |
| `AddresseeName` | Addressee name. |
| `AddresseeAddress` | Addressee address. |
| `AddresseePostalCode` | Addressee postal code. |
| `AddresseeCity` | Addressee city. |
| `AddresseeCountryName` | Addressee country name. Prohibited use when AddresseeCountry is set as home country. |
| `AddresseeCountry` | class Country. Addressee country. |
| `AddresseeGLN` | Addressee GLN. |
| `RecipientName` | Recipient name. |
| `RecipientAddress` | Recipient address. |
| `RecipientPostalCode` | Recipient postal code. |
| `RecipientCity` | Recipient city. |
| `RecipientCountryName` | Recipient country name. Prohibited use when RecipientCountry is set as home country. |
| `RecipientCountry` | class Country. Recipient country. |
| `RecipientGLN` | Addressee GLN. |
| `Rabate` | Rabate percent. |
| `ExchangeRate` | Exchange rate. |
| `DocumentReference` | Document reference. |
| `PaymentReference` | Payment reference. Readonly. |
| `Currency` | class Currency. Currency. |
| `Analytic` | class Analytic. Analytic. |
| `Document` | class Document. Document. Readonly. |
| `IssuedInvoiceReportTemplate` | class ReportTemplate. Report settings for issued invoices:   IR – for issued invoice, DP – for credit note, UP – for issued invoice with order for payment.   Report settings for proforma invoices:   PR – for proforma invoice, PUPN – for proforma invoice with order for payment. |
| `DeliveryNoteReportTemplate` | class ReportTemplate. Report settings for delivery note:   DO – for delivery note |
| `Status` | Issued invoice and proforma invoice status:   O – Draft, I - Issued  Readonly. |
| `DescriptionAbove` | The description that appears on issued invoice and proforma invoice above. |
| `DescriptionBelow` | The description that appears on issued invoice and proforma invoice below. |
| `DeliveryNoteDescriptionAbove` | The description that appears on delivery note above. |
| `DeliveryNoteDescriptionBelow` | The description that appears on delivery note below. |
| `Notes` | Notes. |
| `Employee` | class Employee. Employee. |
| `PricesOnInvoice` | Price calculation type(VAT):   D - VAT is included in the price N - VAT is added to the prices |
| `RecurringInvoice` | Recurring Invoice:   D – yes, N – no. |
| `InvoiceForPeriod` | Invoice for period:   D – yes, N – no. |
| `InvoiceAttachment` | class DocumentAttachment. Invoice attachment (PDF invoice document). |
| `EInvoiceAttachment` | class DocumentAttachment. e-invoice XML file. |
| `InvoiceType` | Input type:   R – issued invoice, P – proforma invoice. |
| `OriginalDocumentType` | Source document type for e-invoice:   IV - invoice AAB – proforma invoice AAK – delivery note CD – credit note CT - contract ON - purchase order VN - sales order AEP - project ALO - recipient GC - public tender ATS - object |
| `OriginalDocumentDate` | Source document date for e-invoice. |
| `PurposeCode` | class PurposeCode. Purpose code for e-invoice and invoice with order for payment. |
| `PaymentStatus` | Payment status:   Placan – Paid DelnoPlacanZapadel – Partially paid, Overdue DelnoPlacanNezapadel – Partially paid, Not yet due NeplacanZapadel – Unpaid, Overdue NeplacanNezapadel – Unpaid, Not yet due Osnutek – Draft Avans – Advance payment  Readonly. |
| `InvoiceValue` | Invoice value (domestic currency). Readonly. |
| `PaidValue` | Paid value (domestic currency). Readonly. |
| `AssociationWithStock` | Association With Issue From Stock:   N – no D – yes |
| `IssuedInvoiceRows` | Invoice rows. List of IssuedInvoiceRow. |
| `IssuedInvoicePaymentMethods` | Payment methods. List of IssuedInvoicePaymentMethod. |
| `IssuedInvoiceAdditionalSourceDocument` | Additional source documents. List of IssuedInvoiceAdditionalSourceDocument. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetIssuedInvoiceAttachments

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoices/{issuedInvoiceId}/attachments`

Returns all attachments for a given issued invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoices-issuedInvoiceId-attachments)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoiceId` | issuedInvoiceId id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Capacity` |  |
| `Count` |  |
| `Item` |  |

---

### GetIssuedInvoicePaymentMethods

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoices/paymentmethods`

Returns all payment methods for given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoices-paymentmethods)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of PaymentMethodSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetIssuedInvoices

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoices`

Returns all issued invoices for given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoices)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `CustomerID` | Customer id. |
| `CustomerName` | Customer Name. |
| `AnalyticsID` | Analytics id. |
| `CurrencyId` | Currency id. |
| `InvoiceType` | Invoice type. Mandatory filter value. |
| `InvoiceNumber` | Invoice number. |
| `Year` | Year. |
| `DateIssuedFrom` | Date issued from. |
| `DateIssuedTo` | Date issued to. |
| `DateDueFrom` | Date due from. |
| `DateDueTo` | Date due to. |
| `DateTransactionFrom` | Date transaction from. |
| `DateTransactionTo` | Date transaction to. |
| `Status` | Status. |
| `PaymentStatus` | Payment Status. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of IssuedInvoiceSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetIssuedInvoicesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoices/synccandidates`

Returns issued invoices for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoices-synccandidates)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `RecordDtModifiedFrom` | RecordDtModifiedFrom - if set return only records last changed after given date time. |
| `RecordDtModifiedTo` | RecordDtModifiedTo - if set return only records last changed before given date time. |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of SyncCandidate. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### UpdateIssuedInvoice

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/issuedinvoices/{issuedInvoiceId}`

Updates issued invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-issuedinvoices-issuedInvoiceId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoiceId` | issuedInvoice id |
| `issuedInvoice` | New issuedInvoice data. |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Version` |  |
| `Content` |  |
| `StatusCode` |  |
| `ReasonPhrase` |  |
| `Headers` |  |
| `RequestMessage` |  |
| `IsSuccessStatusCode` |  |

---
