# JournalType

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/JournalType](https://moj.minimax.si/SI/API/Home/ModuleDetails/JournalType)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetJournalTypeByCode](#getjournaltypebycode) | Returns a journal type for its code. |
| 2 | 🟢 `GET` | [GetJournalTypeByID](#getjournaltypebyid) | Returns a journal type for its id. |
| 3 | 🟢 `GET` | [GetJournalTypes](#getjournaltypes) | Returns all journal types. |
| 4 | 🟢 `GET` | [GetJournalTypesSyncCandidates](#getjournaltypessynccandidates) | Returns journal types for sync. |

## Kazalo metod

- 🟢 [GetJournalTypeByCode](#getjournaltypebycode)
- 🟢 [GetJournalTypeByID](#getjournaltypebyid)
- 🟢 [GetJournalTypes](#getjournaltypes)
- 🟢 [GetJournalTypesSyncCandidates](#getjournaltypessynccandidates)

---

## Podrobnosti metod

### GetJournalTypeByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journaltypes/code({code})`

Returns a journal type for its code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journaltypes-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `code` | JournalType code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `JournalTypeId` | Journal type id. |
| `Code` | Journal type code. |
| `DisplayCode` | Journal type display code. |

---

### GetJournalTypeByID

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journaltypes/{journalTypeId}`

Returns a journal type for its id.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journaltypes-journalTypeId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `journalTypeId` | journalType id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `JournalTypeId` | Journal type id. |
| `Code` | Journal type code. |
| `DisplayCode` | Journal type display code. |

---

### GetJournalTypes

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journaltypes`

Returns all journal types.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journaltypes)

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
| `Rows` | Returned rows. List of JournalType. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetJournalTypesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journaltypes/synccandidates`

Returns journal types for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journaltypes-synccandidates)

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
