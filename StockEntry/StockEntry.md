# StockEntry

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/StockEntry](https://moj.minimax.si/SI/API/Home/ModuleDetails/StockEntry)  
> **Generirano:** 25. 04. 2026 ob 12:16  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddStockEntry](#addstockentry) | Adds a new stock entry. |
| 2 | 🔴 `DELETE` | [DeleteStockEntry](#deletestockentry) | Deletes stock entry. |
| 3 | 🟢 `GET` | [GetCustomActionStockEntry](#getcustomactionstockentry) | Performs a custom action on stock entry. 
 Available actionName values: 
getDeliveryNotepdf |
| 4 | 🟢 `GET` | [GetStockEntries](#getstockentries) | Returns all stock entries for given organisation. |
| 5 | 🟢 `GET` | [GetStockEntry](#getstockentry) | Returns stock entry. |
| 6 | 🟡 `PUT` | [PutCustomActionStockEntry](#putcustomactionstockentry) | Performs a custom action on stock entry.
 Available actionName values: 
confirm
cancelConfirmation |
| 7 | 🟡 `PUT` | [UpdateStockEntry](#updatestockentry) | Updates stock entry. |

## Kazalo metod

- 🔵 [AddStockEntry](#addstockentry)
- 🔴 [DeleteStockEntry](#deletestockentry)
- 🟢 [GetCustomActionStockEntry](#getcustomactionstockentry)
- 🟢 [GetStockEntries](#getstockentries)
- 🟢 [GetStockEntry](#getstockentry)
- 🟡 [PutCustomActionStockEntry](#putcustomactionstockentry)
- 🟡 [UpdateStockEntry](#updatestockentry)

---

## Podrobnosti metod

### AddStockEntry

🔵 **POST** &nbsp;`api/orgs/{organisationId}/stockentry`

Adds a new stock entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-stockentry)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `stockEntry` | stock entry |

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

### DeleteStockEntry

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/stockentry/{stockEntryId}`

Deletes stock entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-stockentry-stockEntryId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `stockEntryId` | stock entry id |

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

### GetCustomActionStockEntry

🟢 **GET** &nbsp;`api/orgs/{organisationId}/stockentry/{stockEntryId}/actions/{actionName}?rowVersion={rowVersion}`

Performs a custom action on stock entry. 
 Available actionName values: 
getDeliveryNotepdf

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-stockentry-stockEntryId-actions-actionName_rowVersion)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id |
| `stockEntryId` | Order id |
| `rowVersion` | Row version is used for concurrency check. |
| `actionName` | Available actionName values: {"getDeliveryNotepdf"} |

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

### GetStockEntries

🟢 **GET** &nbsp;`api/orgs/{organisationId}/stockentry`

Returns all stock entries for given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-stockentry)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `StockEntryType` | StockEntry Type. |
| `StockEntrySubtype` | StockEntry Subtype. |
| `Status` | StockEntry Status. |
| `AnalyticId` | Analytic ID. |
| `DateFrom` | Date from. |
| `DateTo` | Date to. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of StockEntrySearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetStockEntry

🟢 **GET** &nbsp;`api/orgs/{organisationId}/stockentry/{stockEntryId}`

Returns stock entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-stockentry-stockEntryId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `stockEntryId` | stock entry id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `StockEntryId` | Stock entry id. |
| `StockEntryType` | Stock entry type:
   P - Receipt I - Issue L - Own use |
| `StockEntrySubtype` | Stock entry subtype:
   S – Suplier/Client P – Production L - Storage R – Storage to Client/Supplier |
| `Date` | Stock entry date. |
| `Number` | Stock entry number. Readonly. |
| `Customer` | class Customer. Customer. |
| `Analytic` | class Analytic. Analytic. |
| `Rabate` | Rabate percent. |
| `Description` | Description. |
| `ValueOfMaterialAndGoods` | Value of material and goods. |
| `ValueOfRelatedCosts` | Value of related costs. |
| `PercentOfDirectCostsOfPurchase` | Percent of related costs of purchase. |
| `ValueOfReceipt` | Value of receipt. |
| `Currency` | class Currency. Currency. |
| `ExchangeRate` | Exchange rate. |
| `OriginalDocumentType` | Only for miniMAX SI
  Source document type for e-delivery note:
   AAK – delivery note ON - purchase order VN – sales order |
| `OriginalDocumentDate` | Only for miniMAX SI
  Source document date for e-delivery note |
| `DeliveryNoteReportTemplate` | class ReportTemplate. Report settings for delivery note:
   DO – for delivery note |
| `DeliveryNoteDescriptionAbove` | The description that appears on delivery note above. |
| `DeliveryNoteDescriptionBelow` | The description that appears on delivery note below. |
| `AddresseeName` | Addressee name. |
| `AddresseeGLN` | Addressee GLN. |
| `AddresseeAddress` | Addressee address. |
| `AddresseePostalCode` | Addressee postal code. |
| `AddresseeCity` | Addressee city. |
| `AddresseeCountryName` | Addressee country name. Prohibited use when AddresseeCountry is set as home country. |
| `AddresseeCountry` | class Country. Addressee country. |
| `RecipientName` | Recipient name. |
| `RecipientGLN` | Recipient GLN. |
| `RecipientAddress` | Recipient address. |
| `RecipientPostalCode` | Recipient postal code. |
| `RecipientCity` | Recipient city. |
| `RecipientCountryName` | Recipient country name. Prohibited use when RecipientCountry is set as home country. |
| `RecipientCountry` | class Country. Recipient country. |
| `Status` | Stock entry status:
   P – Confirmed, O – Draft |
| `Account` | class Account. Account. |
| `AssociationWithIssuedInvoice` | Association With Issued invoice:
   N – no D – yes |
| `StockEntryRows` | Stock entry rows. List of StockEntryRow. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### PutCustomActionStockEntry

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/stockentry/{stockEntryId}/actions/{actionName}?rowVersion={rowVersion}`

Performs a custom action on stock entry.
 Available actionName values: 
confirm
cancelConfirmation

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-stockentry-stockEntryId-actions-actionName_rowVersion)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id |
| `stockEntryId` | StockEntry id |
| `rowVersion` | Row version is used for concurrency check. |
| `actionName` | Available actionName values: {"confirm", "cancelConfirmation"} |

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

### UpdateStockEntry

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/stockentry/{stockEntryId}`

Updates stock entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-stockentry-stockEntryId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `stockEntryId` | stock entry id |
| `stockEntry` | New stock entry data. |

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
