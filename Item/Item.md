# Item

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Item](https://moj.minimax.si/SI/API/Home/ModuleDetails/Item)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddItem](#additem) | Adds a new item. |
| 2 | 🔴 `DELETE` | [DeleteItem](#deleteitem) | Deletes item. |
| 3 | 🟢 `GET` | [GetItem](#getitem) | Returns an item. |
| 4 | 🟢 `GET` | [GetItemByCode](#getitembycode) | Returns an item with given code. |
| 5 | 🟢 `GET` | [GetItems](#getitems) | Returns all items for the given organization. |
| 6 | 🟢 `GET` | [GetItemsData](#getitemsdata) | Returns items title, code, price and unit of measurement for the given item. |
| 7 | 🟢 `GET` | [GetItemsSettings](#getitemssettings) | Returns items settings for given orgaisation. |
| 8 | 🟢 `GET` | [GetItemsSyncCandidates](#getitemssynccandidates) | Returns items for sync. |
| 9 | 🟢 `GET` | [GetPriceLists](#getpricelists) | Returns item data including selling price (with and without VAT) for combination of given parameters – warehouse and ite |
| 10 | 🟡 `PUT` | [UpdateItem](#updateitem) | Updates item. |

## Kazalo metod

- 🔵 [AddItem](#additem)
- 🔴 [DeleteItem](#deleteitem)
- 🟢 [GetItem](#getitem)
- 🟢 [GetItemByCode](#getitembycode)
- 🟢 [GetItems](#getitems)
- 🟢 [GetItemsData](#getitemsdata)
- 🟢 [GetItemsSettings](#getitemssettings)
- 🟢 [GetItemsSyncCandidates](#getitemssynccandidates)
- 🟢 [GetPriceLists](#getpricelists)
- 🟡 [UpdateItem](#updateitem)

---

## Podrobnosti metod

### AddItem

🔵 **POST** &nbsp;`api/orgs/{organisationId}/items`

Adds a new item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-items)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `item` | item |

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

### DeleteItem

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/items/{itemId}`

Deletes item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-items-itemId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `itemId` | item id |

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

### GetItem

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items/{itemId}`

Returns an item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items-itemId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `itemId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `ItemId` | Item id. |
| `Name` | Item name. |
| `Code` | Item code. |
| `EANCode` | EAN code. |
| `Description` | Item description. |
| `ItemType` | Possible values: (B, M, P, I, S, A, AS). Item type:   B – Goods, M – Material, P - Semifinished product, I – Product, S – Services, A - Advance payment, AS - Pre payments for services |
| `StocksManagedOnlyByQuantity` | Possible values: (D, N). Defines whether are stocks managed only by quantity.   N - stocks are managed by quantity and value D - stocks are managed only by quantity    Default value: N. |
| `UnitOfMeasurement` | Item unit of measurement. |
| `MassPerUnit` | Mass per unit. |
| `ProductGroup` | class ProductGroup. Item product group. |
| `VatRate` | class VatRate. Item VAT rate. |
| `Price` | Item selling price. |
| `RebatePercent` | Margin percent. |
| `Usage` | Possible values: (D, N). Usage:   D – yes, N – no. |
| `Currency` | class Currency. Selling price currency. |
| `SerialNumbers` | Possible values: (D, N). SerialNumbers:   D – yes, N – no. |
| `BatchNumbers` | Possible values: (D, N). BatchNumbers:   D – yes, N – no. |
| `RevenueAccountDomestic` | class Account. Domestic market revenue account. |
| `RevenueAccountEU` | class Account. Revenue account for EU markets. |
| `RevenueAccountOutsideEU` | class Account. Revenue account outside EU markets. |
| `StocksAccount` | class Account. Stock account. |
| `ReliefByCompositeFromWarehouse` | Possible values: (D, N). Article relief by composite when issuing from warehouse:   D – yes, N – no. |
| `ReliefByCompositeFromIssuedInvoice` | Possible values: (D, N). Article relief by composite from issued invoice:   D – yes, N – no. |
| `Composite` | Composite rows. List of ItemComposite. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetItemByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items/code({code})`

Returns an item with given code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `code` | item code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `ItemId` | Item id. |
| `Name` | Item name. |
| `Code` | Item code. |
| `EANCode` | EAN code. |
| `Description` | Item description. |
| `ItemType` | Possible values: (B, M, P, I, S, A, AS). Item type:   B – Goods, M – Material, P - Semifinished product, I – Product, S – Services, A - Advance payment, AS - Pre payments for services |
| `StocksManagedOnlyByQuantity` | Possible values: (D, N). Defines whether are stocks managed only by quantity.   N - stocks are managed by quantity and value D - stocks are managed only by quantity    Default value: N. |
| `UnitOfMeasurement` | Item unit of measurement. |
| `MassPerUnit` | Mass per unit. |
| `ProductGroup` | class ProductGroup. Item product group. |
| `VatRate` | class VatRate. Item VAT rate. |
| `Price` | Item selling price. |
| `RebatePercent` | Margin percent. |
| `Usage` | Possible values: (D, N). Usage:   D – yes, N – no. |
| `Currency` | class Currency. Selling price currency. |
| `SerialNumbers` | Possible values: (D, N). SerialNumbers:   D – yes, N – no. |
| `BatchNumbers` | Possible values: (D, N). BatchNumbers:   D – yes, N – no. |
| `RevenueAccountDomestic` | class Account. Domestic market revenue account. |
| `RevenueAccountEU` | class Account. Revenue account for EU markets. |
| `RevenueAccountOutsideEU` | class Account. Revenue account outside EU markets. |
| `StocksAccount` | class Account. Stock account. |
| `ReliefByCompositeFromWarehouse` | Possible values: (D, N). Article relief by composite when issuing from warehouse:   D – yes, N – no. |
| `ReliefByCompositeFromIssuedInvoice` | Possible values: (D, N). Article relief by composite from issued invoice:   D – yes, N – no. |
| `Composite` | Composite rows. List of ItemComposite. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetItems

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items`

Returns all items for the given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `SearchString` | Search string. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of ItemSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetItemsData

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items/itemsdata`

Returns items title, code, price and unit of measurement for the given item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items-itemsdata)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `WarehouseId` | WarehouseId |
| `CustomerId` | CustomerId |
| `ItemId` | ItemId |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of ItemData. |
| `ValidationMessages` | Validation messages. List of mMApiValidationMessage. |

---

### GetItemsSettings

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items/settings`

Returns items settings for given orgaisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items-settings)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `PricesIncludeVAT` | If prices include VAT then D else N. |

---

### GetItemsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items/synccandidates`

Returns items for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items-synccandidates)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `SyncMode` | SyncMode - change the search behaviour (advanced feature). |
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

### GetPriceLists

🟢 **GET** &nbsp;`api/orgs/{organisationId}/items/pricelists`

Returns item data including selling price (with and without VAT) for combination of given parameters – warehouse and item or custumer and item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-items-pricelists)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `WarehouseId` | WarehouseId |
| `CustomerId` | CustomerId |
| `ItemId` | ItemId |
| `Mode` | Parameter is not required. If parameter is set to 1 the function returns only items that are included in selected warehouse or used for selected customer. |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of ItemPriceListItem. |
| `ValidationMessages` | Validation messages. List of mMApiValidationMessage. |

---

### UpdateItem

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/items/{itemId}`

Updates item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-items-itemId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `itemId` | item id |
| `item` | New item data. |

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
