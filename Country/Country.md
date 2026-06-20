# Country

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Country](https://moj.minimax.si/SI/API/Home/ModuleDetails/Country)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetCountries](#getcountries) | Returns all countries. |
| 2 | 🟢 `GET` | [GetCountriesSyncCandidates](#getcountriessynccandidates) | Returns countries for sync. |
| 3 | 🟢 `GET` | [GetCountryByCode](#getcountrybycode) | Returns a country for its code. |
| 4 | 🟢 `GET` | [GetCountryByID](#getcountrybyid) | Returns a country for its id. |

## Kazalo metod

- 🟢 [GetCountries](#getcountries)
- 🟢 [GetCountriesSyncCandidates](#getcountriessynccandidates)
- 🟢 [GetCountryByCode](#getcountrybycode)
- 🟢 [GetCountryByID](#getcountrybyid)

---

## Podrobnosti metod

### GetCountries

🟢 **GET** &nbsp;`api/orgs/{organisationId}/countries`

Returns all countries.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-countries)

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
| `Rows` | Returned rows. List of Country. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetCountriesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/countries/synccandidates`

Returns countries for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-countries-synccandidates)

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

### GetCountryByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/countries/code({code})`

Returns a country for its code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-countries-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `code` | Country code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CountryId` | Country id. |
| `Code` | Country code. |
| `Name` | Country name. |
| `Currency` | class Currency. Country currency. |

---

### GetCountryByID

🟢 **GET** &nbsp;`api/orgs/{organisationId}/countries/{countryId}`

Returns a country for its id.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-countries-countryId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `countryId` | country id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CountryId` | Country id. |
| `Code` | Country code. |
| `Name` | Country name. |
| `Currency` | class Currency. Country currency. |

---
