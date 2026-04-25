# Order

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Order](https://moj.minimax.si/SI/API/Home/ModuleDetails/Order)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddOrder](#addorder) | Adds a new order. |
| 2 | 🔴 `DELETE` | [DeleteOrder](#deleteorder) | Deletes order. |
| 3 | 🟢 `GET` | [GetCustomActionOrder](#getcustomactionorder) | Performs a custom action on order. 
 Available actionName values: 
getorderpdf |
| 4 | 🟢 `GET` | [GetOrder](#getorder) | Returns an order. |
| 5 | 🟢 `GET` | [GetOrders](#getorders) | Returns all orders for given organization. |
| 6 | 🟢 `GET` | [GetOrdersSyncCandidates](#getorderssynccandidates) | Returns orders for sync. |
| 7 | 🟡 `PUT` | [PutCustomActionOrder](#putcustomactionorder) | Performs a custom action on order.
 Available actionName values: 
confirm
cancelConfirmation
complete
cancelCompletion
 |
| 8 | 🟡 `PUT` | [UpdateOrder](#updateorder) | Updates order. |

## Kazalo metod

- 🔵 [AddOrder](#addorder)
- 🔴 [DeleteOrder](#deleteorder)
- 🟢 [GetCustomActionOrder](#getcustomactionorder)
- 🟢 [GetOrder](#getorder)
- 🟢 [GetOrders](#getorders)
- 🟢 [GetOrdersSyncCandidates](#getorderssynccandidates)
- 🟡 [PutCustomActionOrder](#putcustomactionorder)
- 🟡 [UpdateOrder](#updateorder)

---

## Podrobnosti metod

### AddOrder

🔵 **POST** &nbsp;`api/orgs/{organisationId}/orders`

Adds a new order.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-orders)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `order` | order |

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

### DeleteOrder

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/orders/{orderId}`

Deletes order.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-orders-orderId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `orderId` | order id |

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

### GetCustomActionOrder

🟢 **GET** &nbsp;`api/orgs/{organisationId}/orders/{orderId}/actions/{actionName}?rowVersion={rowVersion}`

Performs a custom action on order. 
 Available actionName values: 
getorderpdf

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-orders-orderId-actions-actionName_rowVersion)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id |
| `orderId` | Order id |
| `rowVersion` | Row version is used for concurrency check. |
| `actionName` | Available actionName values: {"getorderpdf"} |

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

### GetOrder

🟢 **GET** &nbsp;`api/orgs/{organisationId}/orders/{orderId}`

Returns an order.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-orders-orderId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id |
| `orderId` | Order id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `OrderId` | Order id. |
| `ReceivedIssued` | Possible values: (P, I). Order type:   I – issued order, P – recieved order. |
| `Year` | Order year. Readonly. |
| `Number` | Order number. Readonly. |
| `Date` | Order date. |
| `Customer` | class Customer. Customer. |
| `CustomerName` | Customer name. |
| `CustomerAddress` | Customer address. |
| `CustomerPostalCode` | Customer postal code. |
| `CustomerCity` | Customer city. |
| `CustomerCountry` | class Country. Customer country. |
| `CustomerCountryName` | Customer country name. |
| `RecipientName` | Recipient name. |
| `RecipientAddress` | Recipient address. |
| `RecipientPostalCode` | Recipient postal code. |
| `RecipientCity` | Recipient city. |
| `RecipientCountryName` | Recipient country name. Prohibited use when RecipientCountry is set as home country. |
| `RecipientCountry` | class Country. Recipient country. |
| `Analytic` | class Analytic. Analytic. |
| `DueDate` | Due date. |
| `Reference` | Reference. |
| `Currency` | class Currency. Currency. |
| `Notes` | Notes. |
| `DateConfirmed` | Order confirmation date. Readonly. |
| `DateCompleted` | Order termination date. Readonly. |
| `DateCanceled` | Order Invalidation date. Readonly. |
| `Status` | Order status:   P – Confirmed, O – Draft, Z – Terminated, R - Invalidated  Readonly. |
| `DescriptionAbove` | The description that appears on order print above. |
| `DescriptionBelow` | The description that appears on order print below. |
| `ReportTemplate` | class ReportTemplate. Report settings for orders:   IN – for issued orders, PN – for received orders |
| `OrderRows` | Order rows. List of OrderRow. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetOrders

🟢 **GET** &nbsp;`api/orgs/{organisationId}/orders`

Returns all orders for given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-orders)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `CustomerID` | Customer id. |
| `DateFrom` | Date from. |
| `DateTo` | Date to. |
| `DateConfirmedFrom` | Date confirmed from. |
| `DateConfirmedTo` | Date confirmed to. |
| `DateCompletedFrom` | Date completed from. |
| `DateCompletedTo` | Date completed to. |
| `DateCanceledFrom` | Date canceled from. |
| `DateCanceledTo` | Date canceled to. |
| `ReceivedIssued` | Received/Issued. |
| `Year` | Year. |
| `Number` | Number. |
| `AnalyticsID` | Analytics id. |
| `Reference` | Reference. |
| `Status` | Status. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of OrderSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetOrdersSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/orders/synccandidates`

Returns orders for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-orders-synccandidates)

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

### PutCustomActionOrder

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/orders/{orderId}/actions/{actionName}?rowVersion={rowVersion}`

Performs a custom action on order.
 Available actionName values: 
confirm
cancelConfirmation
complete
cancelCompletion
invalidate
cancelInvalidation
createissuedinvoice
generatepdf

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-orders-orderId-actions-actionName_rowVersion)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id |
| `orderId` | Order id |
| `rowVersion` | Row version is used for concurrency check. |
| `actionName` | Available actionName values: {"confirm", "cancelConfirmation", "complete", "cancelCompletion", "invalidate", "cancelInvalidation", "createissuedinvoice"} |

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

### UpdateOrder

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/orders/{orderId}`

Updates order.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-orders-orderId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `orderId` | order id |
| `order` | New order data. |

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
