# PurposeCode

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/PurposeCode](https://moj.minimax.si/SI/API/Home/ModuleDetails/PurposeCode)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetPurposeCodeByCode](#getpurposecodebycode) | Returns a purpose code for its code. |
| 2 | 🟢 `GET` | [GetPurposeCodeByID](#getpurposecodebyid) | Returns a purpose code for its ID. |
| 3 | 🟢 `GET` | [GetPurposeCodes](#getpurposecodes) | Returns all purpose codes. |
| 4 | 🟢 `GET` | [GetPurposeCodesSyncCandidates](#getpurposecodessynccandidates) | Returns purpose codes for sync. |

## Kazalo metod

- 🟢 [GetPurposeCodeByCode](#getpurposecodebycode)
- 🟢 [GetPurposeCodeByID](#getpurposecodebyid)
- 🟢 [GetPurposeCodes](#getpurposecodes)
- 🟢 [GetPurposeCodesSyncCandidates](#getpurposecodessynccandidates)

---

## Podrobnosti metod

### GetPurposeCodeByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/purpose-codes/code({code})`

Returns a purpose code for its code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-purpose-codes-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `code` | Purposecode code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `PurposeCodeId` | Purpose code id |
| `Code` | Code. |
| `Description` | Purpose code description. |

---

### GetPurposeCodeByID

🟢 **GET** &nbsp;`api/orgs/{organisationId}/purpose-codes/{purposeCodeId}`

Returns a purpose code for its ID.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-purpose-codes-purposeCodeId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `purposeCodeId` | purpose code id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `PurposeCodeId` | Purpose code id |
| `Code` | Code. |
| `Description` | Purpose code description. |

---

### GetPurposeCodes

🟢 **GET** &nbsp;`api/orgs/{organisationId}/purpose-codes`

Returns all purpose codes.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-purpose-codes)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of PurposeCode. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetPurposeCodesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/purpose-codes/synccandidates`

Returns purpose codes for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-purpose-codes-synccandidates)

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
