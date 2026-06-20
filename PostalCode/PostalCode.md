# PostalCode

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/PostalCode](https://moj.minimax.si/SI/API/Home/ModuleDetails/PostalCode)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetPostalCodeByID](#getpostalcodebyid) | Returns a postal code by id. |
| 2 | 🟢 `GET` | [GetPostalCodesForCounty](#getpostalcodesforcounty) | Returns all postal codes for given country. |
| 3 | 🟢 `GET` | [GetPostalCodesSyncCandidates](#getpostalcodessynccandidates) | Returns postal codes for sync. |

## Kazalo metod

- 🟢 [GetPostalCodeByID](#getpostalcodebyid)
- 🟢 [GetPostalCodesForCounty](#getpostalcodesforcounty)
- 🟢 [GetPostalCodesSyncCandidates](#getpostalcodessynccandidates)

---

## Podrobnosti metod

### GetPostalCodeByID

🟢 **GET** &nbsp;`api/orgs/{organisationId}/postalcodes/{postalCodeId}`

Returns a postal code by id.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-postalcodes-postalCodeId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `postalCodeId` | Postal code id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `PostalCodeId` | Postal code id. |
| `Code` | Code. |
| `City` | City. |
| `Country` | class Country. Country. |

---

### GetPostalCodesForCounty

🟢 **GET** &nbsp;`api/orgs/{organisationId}/postalcodes/countries/{countryId}`

Returns all postal codes for given country.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-postalcodes-countries-countryId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `countryId` |  |
| `SearchString` | Search string. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of PostalCode. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetPostalCodesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/postalcodes/synccandidates`

Returns postal codes for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-postalcodes-synccandidates)

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
