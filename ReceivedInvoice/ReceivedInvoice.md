# ReceivedInvoice

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/ReceivedInvoice](https://moj.minimax.si/SI/API/Home/ModuleDetails/ReceivedInvoice)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddAttachment](#addattachment) | Adds an attachment to a given received invoice. |
| 2 | 🔵 `POST` | [AddReceivedInvoice](#addreceivedinvoice) | Adds a new received invoice. |
| 3 | 🔴 `DELETE` | [DeleteReceivedInvoice](#deletereceivedinvoice) | Deletes received invoice. |
| 4 | 🟢 `GET` | [GetAttachments](#getattachments) | Returns all attachments for a given received invoice. |
| 5 | 🟢 `GET` | [GetReceivedInvoice](#getreceivedinvoice) | Returns a received invoice. |
| 6 | 🟢 `GET` | [GetReceivedInvoices](#getreceivedinvoices) | Returns all received invoices for the given organization. |
| 7 | 🟡 `PUT` | [UpdateReceivedInvoice](#updatereceivedinvoice) | Updates received invoice. |

## Kazalo metod

- 🔵 [AddAttachment](#addattachment)
- 🔵 [AddReceivedInvoice](#addreceivedinvoice)
- 🔴 [DeleteReceivedInvoice](#deletereceivedinvoice)
- 🟢 [GetAttachments](#getattachments)
- 🟢 [GetReceivedInvoice](#getreceivedinvoice)
- 🟢 [GetReceivedInvoices](#getreceivedinvoices)
- 🟡 [UpdateReceivedInvoice](#updatereceivedinvoice)

---

## Podrobnosti metod

### AddAttachment

🔵 **POST** &nbsp;`api/orgs/{organisationId}/receivedinvoices/{receivedInvoiceId}/attachments`

Adds an attachment to a given received invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-receivedinvoices-receivedInvoiceId-attachments)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `receivedInvoiceId` | receivedInvoiceId id |
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

### AddReceivedInvoice

🔵 **POST** &nbsp;`api/orgs/{organisationId}/receivedinvoices`

Adds a new received invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-receivedinvoices)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `receivedInvoice` | received Invoice |

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

### DeleteReceivedInvoice

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/receivedinvoices/{receivedInvoiceId}`

Deletes received invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-receivedinvoices-receivedInvoiceId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `receivedInvoiceId` | receivedInvoiceId id |

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

### GetAttachments

🟢 **GET** &nbsp;`api/orgs/{organisationId}/receivedinvoices/{receivedInvoiceId}/attachments`

Returns all attachments for a given received invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-receivedinvoices-receivedInvoiceId-attachments)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `receivedInvoiceId` | receivedInvoiceId id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Capacity` |  |
| `Count` |  |
| `Item` |  |

---

### GetReceivedInvoice

🟢 **GET** &nbsp;`api/orgs/{organisationId}/receivedinvoices/{receivedInvoiceId}`

Returns a received invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-receivedinvoices-receivedInvoiceId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `receivedInvoiceId` | receivedInvoiceId id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `ReceivedInvoiceId` | Received Invoice Id |
| `Year` | Invoice year. Readonly. |
| `InvoiceNumber` | Invoice number. Readonly. |
| `DocumentNumbering` | class DocumentNumbering. Document numbering. |
| `DocumentReference` | Document reference |
| `Customer` | class Customer. Customer. |
| `Employee` | class Employee. Employee. |
| `Analytic` | class Analytic. Analytic. |
| `Currency` | class Currency. Currency. |
| `DateIssued` | Invoice date |
| `DateTransaction` | Date of transaction |
| `DateDue` | Invoice due date |
| `DateReceived` | Received date |
| `InvoiceAmount` | Amount of invoice |
| `InvoiceAmountDomesticCurrency` | Amount of invoice in domestic currency |
| `Status` | Received invoice status:   P – Confirmed, O – Draft, Z - Rejected,  Readonly. |
| `BankAccount` | class BankAccount. Customer Bank Account |
| `PaymentReferenceType` | Payment Reference Type:   SI, RF, |
| `PaymentReferenceModel` | Payment reference model |
| `PaymentReferenceNumber` | Payment reference number |
| `Notes` | Notes |
| `PaymentType` | Payment type:   D – Payment order, N – No payment order, Z – Paid by private undertaking, P – Paid by employee, R – Using another account, B – Cash book, |
| `RevenueExpense` | Expense when paid by cash book |
| `CashRegister` | Cash register when paid by cash book |
| `DateExpense` | Date of expense when paid by cash book |
| `RecurringInvoice` | Recurring Invoice:   D – yes, N – no, |
| `PaymentStatus` | Payment status:   Placan – Paid, DelnoPlacanZapadel – Partially paid, Overdue DelnoPlacanNezapadel – Partially paid, Not yet due NeplacanZapadel – Unpaid, Overdue, NeplacanNezapadel – Unpaid, Not yet due Osnutek – Draft, Avans – Advance payment  Readonly. |
| `InvoiceValue` | Invoice value Readonly. |
| `PaidValue` | Paid value Readonly. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetReceivedInvoices

🟢 **GET** &nbsp;`api/orgs/{organisationId}/receivedinvoices`

Returns all received invoices for the given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-receivedinvoices)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `CustomerID` | Customer id. |
| `CustomerName` | Customer Name. |
| `InvoiceNumber` | Invoice Number. |
| `Status` | Status. |
| `DateIssuedFrom` | Invoice date from. |
| `DateIssuedTo` | Invoice date to. |
| `DocumentReference` | Document Reference. |
| `DateDueFrom` | Date due from. |
| `DateDueTo` | Date due to. |
| `DateTransactionFrom` | Date transaction from. |
| `DateTransactionTo` | Date transaction to. |
| `Year` | Year. |
| `PaymentStatus` | Payment Status. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of ReceivedInvoiceSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### UpdateReceivedInvoice

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/receivedinvoices/{receivedInvoiceId}`

Updates received invoice.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-receivedinvoices-receivedInvoiceId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `receivedInvoiceId` | received Invoice id |
| `receivedInvoice` | New receivedInvoice data. |

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
