# Warehouse

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Warehouse](https://moj.minimax.si/SI/API/Home/ModuleDetails/Warehouse)  
> **Generirano:** 25. 04. 2026 ob 12:16  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddWarehouse](#addwarehouse) | Adds a new warehouse. |
| 2 | 🔴 `DELETE` | [DeleteWarehouse](#deletewarehouse) | Deletes a warehouse. |
| 3 | 🟢 `GET` | [GetWarehouse](#getwarehouse) | Returns a warehouse. |
| 4 | 🟢 `GET` | [GetWarehouses](#getwarehouses) | Returns all warehouses for a given organization. |
| 5 | 🟢 `GET` | [GetWarehousesSyncCandidates](#getwarehousessynccandidates) | Returns warehouses for sync. |
| 6 | 🟡 `PUT` | [UpdateWarehouse](#updatewarehouse) | Updates a warehouse. |

## Kazalo metod

- 🔵 [AddWarehouse](#addwarehouse)
- 🔴 [DeleteWarehouse](#deletewarehouse)
- 🟢 [GetWarehouse](#getwarehouse)
- 🟢 [GetWarehouses](#getwarehouses)
- 🟢 [GetWarehousesSyncCandidates](#getwarehousessynccandidates)
- 🟡 [UpdateWarehouse](#updatewarehouse)

---

## Podrobnosti metod

### AddWarehouse

🔵 **POST** &nbsp;`api/orgs/{organisationId}/warehouses`

Adds a new warehouse.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-warehouses)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `warehouse` | warehouse id |

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

### DeleteWarehouse

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/warehouses/{warehouseId}`

Deletes a warehouse.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-warehouses-warehouseId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `warehouseId` | warehouse id |

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

### GetWarehouse

🟢 **GET** &nbsp;`api/orgs/{organisationId}/warehouses/{warehouseId}`

Returns a warehouse.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-warehouses-warehouseId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `warehouseId` | warehouse id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `WarehouseId` | Warehouse id. |
| `Code` | Warehouse code. |
| `Name` | Warehouse name. |
| `InventoryManagement` | Type of inventory management:   Nabavna – Purchase value, Prodajna – Sales value |
| `InventoryManagementByValue` | Enable selling price input in stocks:   D - yes, N - no |
| `SellingPriceInput` | InventoryManagement only by value:   D - yes, N - no |
| `InventoryBookkeping` | Type of inventory bookkepping:   Nabavna – Purchase value, Prodajna – Sales value |
| `StocksAccount` | class Account. Stocks account. |
| `PDAccount` | class Account. Account for price difference. |
| `VATStandardAccount` | class Account. Account for VAT standard rate. |
| `VATReducedAccount` | class Account. Account for VAT reduced rate. |
| `VATSpecialReducedAccount` | class Account. Account for VAT special reduced rate. |
| `Usage` | Usage:   D - yes, N - no |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetWarehouses

🟢 **GET** &nbsp;`api/orgs/{organisationId}/warehouses`

Returns all warehouses for a given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-warehouses)

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
| `Rows` | Returned rows. List of Warehouse. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetWarehousesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/warehouses/synccandidates`

Returns warehouses for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-warehouses-synccandidates)

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

### UpdateWarehouse

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/warehouses/{warehouseId}`

Updates a warehouse.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-warehouses-warehouseId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `warehouseId` | warehouse id |
| `warehouse` | New warehouse data. |

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
