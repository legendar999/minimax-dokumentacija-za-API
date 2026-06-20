# IssuedInvoicePosting

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/IssuedInvoicePosting](https://moj.minimax.si/SI/API/Home/ModuleDetails/IssuedInvoicePosting)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddIssuedInvoicePosting](#addissuedinvoiceposting) | Adds a new issued invoice posting. |
| 2 | 🟡 `PUT` | [CustomActionIssuedInvoicePosting](#customactionissuedinvoiceposting) | Performs a custom action on IssuesInvoicePosting.
 Available actionName values:
 
issue
issueCancellation |
| 3 | 🔴 `DELETE` | [DeleteIssuedInvoicePosting](#deleteissuedinvoiceposting) | Deletes an issued invoice posting. |
| 4 | 🟢 `GET` | [GetIssuedInvoicePosting](#getissuedinvoiceposting) | Returns an issued invoice posting. |
| 5 | 🟢 `GET` | [GetIssuedInvoicePostingPaymentMethods](#getissuedinvoicepostingpaymentmethods) | Returns all payment methods to be used within IssuedInvoicePosting objects (for given organisation). |
| 6 | 🟢 `GET` | [GetIssuedInvoicePostings](#getissuedinvoicepostings) | Returns issued invoice postings for a given organisation. |

## Kazalo metod

- 🔵 [AddIssuedInvoicePosting](#addissuedinvoiceposting)
- 🟡 [CustomActionIssuedInvoicePosting](#customactionissuedinvoiceposting)
- 🔴 [DeleteIssuedInvoicePosting](#deleteissuedinvoiceposting)
- 🟢 [GetIssuedInvoicePosting](#getissuedinvoiceposting)
- 🟢 [GetIssuedInvoicePostingPaymentMethods](#getissuedinvoicepostingpaymentmethods)
- 🟢 [GetIssuedInvoicePostings](#getissuedinvoicepostings)

---

## Podrobnosti metod

### AddIssuedInvoicePosting

🔵 **POST** &nbsp;`api/orgs/{organisationId}/issuedinvoicepostings`

Adds a new issued invoice posting.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-issuedinvoicepostings)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoicePosting` | issuedInvoicePosting |

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

### CustomActionIssuedInvoicePosting

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/issuedinvoicepostings/{issuedInvoicePostingId}/actions/{actionName}`

Performs a custom action on IssuesInvoicePosting.
 Available actionName values:
 
issue
issueCancellation

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-issuedinvoicepostings-issuedInvoicePostingId-actions-actionName)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id. |
| `issuedInvoicePostingId` | Issued invoice posting id. |
| `actionName` | Available actionName values: {"issue", "issueCancellation"} |

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

### DeleteIssuedInvoicePosting

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/issuedinvoicepostings/{issuedInvoicePostingId}`

Deletes an issued invoice posting.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-issuedinvoicepostings-issuedInvoicePostingId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoicePostingId` | issuedInvoicePosting id |

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

### GetIssuedInvoicePosting

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoicepostings/{issuedInvoicePostingId}`

Returns an issued invoice posting.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoicepostings-issuedInvoicePostingId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `issuedInvoicePostingId` | issuedInvoicePosting id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `IssuedInvoicePostingId` | Issued invoice posting id. |
| `DocumentType` | Document type:
   IZT - daily income IRI - daily income invoice (used for VAT reporting purpuses to additionaly specify VAT, payments, taxes and revenues already included in daily income) IRS - issued invoice AVA - advance payment |
| `Status` | Status:
   O – draft, P - confirmed  Readonly. |
| `Customer` | class Customer. Required and only available on document types:
   daily income invoice issued invoice advance payment |
| `DateTransaction` | Date of transaction. Required and only available on document types:
   issued invoice advance payment |
| `DateDue` | Invoice due date. Required and only available on document types:
   issued invoice |
| `PaymentReference` | Payment reference. Only available on document types:
   issued invoice |
| `Analytic` | class Analytic. Analytic. |
| `Date` | Document date. |
| `Description` | Document. |
| `Currency` | class Currency. Default = home currency. |
| `ExchangeRate` | Default = 1. |
| `ForwardToSEF` | Only for Minimax RS organisations that send data to eFaktura.
  Forwarding VAT data to SEF
  Options:
   Zbirno - Group Posamicno - Individual |
| `SalesValue` | Sales value (without VAT) to be posted for retail. Should be supplied when posting for branch office of type:
   Retail shop - Value retail trade Retail shop - Decoupled |
| `SalesValueVAT` | Sales VAT to be posted for retail. Should be supplied when posting for branch office of type:
   Retail shop - Value retail trade Retail shop - Decoupled |
| `PurchaseValue` | Purchase value to be posted for retail. Should be supplied when posting for branch office of type:
   Retail shop - Value retail trade |
| `IssuedInvoicePostingPaymentMethods` | Payment methods. Only available on document types:
   daily income issued invoice  List of IssuedInvoicePostingPaymentMethod. |
| `IssuedInvoicePostingTaxes` | Taxes. List of IssuedInvoicePostingTax. |
| `IssuedInvoicePostingRevenues` | Revenues. Only available on document types:
   daily income issued invoice  List of IssuedInvoicePostingRevenue. |
| `IssuedInvoicePostingRetailDataForBookkeeping` | Retail data for bookkeeping. Only available on document types:
   daily income issued invoice  class IssuedInvoicePostingRetailDataForBookkeeping. |
| `IssuedInvoicePostingRetailDataForValueBasedStockManagement` | Retail data for value based stock management. Only available on document types:
   daily income issued invoice  class IssuedInvoicePostingRetailDataForValueBasedStockManagement. |
| `IssuedInvoicePostingRetailDataForStockManagement` | Retail data for stock management. Only available on document types:
   daily income issued invoice  class IssuedInvoicePostingRetailDataForStockManagement. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetIssuedInvoicePostingPaymentMethods

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoicepostings/paymentmethods`

Returns all payment methods to be used within IssuedInvoicePosting objects (for given organisation).

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoicepostings-paymentmethods)

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

### GetIssuedInvoicePostings

🟢 **GET** &nbsp;`api/orgs/{organisationId}/issuedinvoicepostings`

Returns issued invoice postings for a given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-issuedinvoicepostings)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `DateFrom` | Optional. Filters from (including) supplied date. |
| `DateTo` | Optional. Filters up to (including) supplied date. |
| `Description` | Optional. Filter by (part of) description. |
| `Status` | Optional. Filters by status. |
| `AnalyticID` | Optional. Filters by analytic. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of IssuedInvoicePostingSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
