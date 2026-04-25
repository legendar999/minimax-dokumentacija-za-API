# ProductGroup

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/ProductGroup](https://moj.minimax.si/SI/API/Home/ModuleDetails/ProductGroup)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddProductGroup](#addproductgroup) | Adds a new product group. |
| 2 | 🔴 `DELETE` | [DeleteProductGroup](#deleteproductgroup) | Deletes a product group. |
| 3 | 🟢 `GET` | [GetProductGroup](#getproductgroup) | Returns a product group. |
| 4 | 🟢 `GET` | [GetProductGroups](#getproductgroups) | Returns all product groups for the given organisation. |
| 5 | 🟢 `GET` | [GetProductGroupsSyncCandidates](#getproductgroupssynccandidates) | Returns product groups for sync. |
| 6 | 🟡 `PUT` | [UpdateProductGroup](#updateproductgroup) | Updates a product group. |

## Kazalo metod

- 🔵 [AddProductGroup](#addproductgroup)
- 🔴 [DeleteProductGroup](#deleteproductgroup)
- 🟢 [GetProductGroup](#getproductgroup)
- 🟢 [GetProductGroups](#getproductgroups)
- 🟢 [GetProductGroupsSyncCandidates](#getproductgroupssynccandidates)
- 🟡 [UpdateProductGroup](#updateproductgroup)

---

## Podrobnosti metod

### AddProductGroup

🔵 **POST** &nbsp;`api/orgs/{organisationId}/productGroups`

Adds a new product group.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-productGroups)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `productGroup` | product group data |

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

### DeleteProductGroup

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/productGroups/{productGroupId}`

Deletes a product group.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-productGroups-productGroupId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `productGroupId` | product group id |

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

### GetProductGroup

🟢 **GET** &nbsp;`api/orgs/{organisationId}/productGroups/{productGroupId}`

Returns a product group.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-productGroups-productGroupId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `productGroupId` | product group id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `ProductGroupId` | ProductGroup id. |
| `Code` | ProductGroup code. |
| `Name` | ProductGroup name |
| `Usage` | Usage:   D – Yes, N – No. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetProductGroups

🟢 **GET** &nbsp;`api/orgs/{organisationId}/productGroups`

Returns all product groups for the given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-productGroups)

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
| `Rows` | Returned rows. List of ProductGroup. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetProductGroupsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/productGroups/synccandidates`

Returns product groups for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-productGroups-synccandidates)

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

### UpdateProductGroup

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/productGroups/{productGroupId}`

Updates a product group.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-productGroups-productGroupId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `productGroupId` | product group id |
| `productGroup` | product group data |

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
