# VatAccountingType

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/VatAccountingType](https://moj.minimax.si/SI/API/Home/ModuleDetails/VatAccountingType)  
> **Generirano:** 25. 04. 2026 ob 12:16  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetVatAccountingTypes](#getvataccountingtypes) | Returns all vat accounting types. |
| 2 | 🟢 `GET` | [GetVatAccountingTypesSyncCandidates](#getvataccountingtypessynccandidates) | Returns vat accounting types for sync. |

## Kazalo metod

- 🟢 [GetVatAccountingTypes](#getvataccountingtypes)
- 🟢 [GetVatAccountingTypesSyncCandidates](#getvataccountingtypessynccandidates)

---

## Podrobnosti metod

### GetVatAccountingTypes

🟢 **GET** &nbsp;`api/orgs/{organisationId}/vataccountingtypes?date={date}`

Returns all vat accounting types.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-vataccountingtypes_date)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation ID |
| `date` | Date Effective From (Date format: yyyy-MM-dd) |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of VatAccountingType. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetVatAccountingTypesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/vataccountingtypes/synccandidates`

Returns vat accounting types for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-vataccountingtypes-synccandidates)

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
