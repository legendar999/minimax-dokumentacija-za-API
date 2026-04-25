# Currency

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Currency](https://moj.minimax.si/SI/API/Home/ModuleDetails/Currency)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetCurrencies](#getcurrencies) | Returns all currencies. |
| 2 | 🟢 `GET` | [GetCurrenciesSyncCandidates](#getcurrenciessynccandidates) | Returns currencies for sync. |
| 3 | 🟢 `GET` | [GetCurrencyByCode](#getcurrencybycode) | Returns a currency for given id. |
| 4 | 🟢 `GET` | [GetCurrencyByID](#getcurrencybyid) | Returns a currency for given id. |
| 5 | 🟢 `GET` | [GetDomesticCurrency](#getdomesticcurrency) | Returns a domestic currency. |

## Kazalo metod

- 🟢 [GetCurrencies](#getcurrencies)
- 🟢 [GetCurrenciesSyncCandidates](#getcurrenciessynccandidates)
- 🟢 [GetCurrencyByCode](#getcurrencybycode)
- 🟢 [GetCurrencyByID](#getcurrencybyid)
- 🟢 [GetDomesticCurrency](#getdomesticcurrency)

---

## Podrobnosti metod

### GetCurrencies

🟢 **GET** &nbsp;`api/orgs/{organisationId}/currencies`

Returns all currencies.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-currencies)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `SearchString` |  |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of Currency. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetCurrenciesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/currencies/synccandidates`

Returns currencies for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-currencies-synccandidates)

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

### GetCurrencyByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/currencies/code({code})`

Returns a currency for given id.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-currencies-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `code` | currency code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CurrencyId` | Currency id. |
| `Code` | Currency code. |
| `Name` | Currency name. |

---

### GetCurrencyByID

🟢 **GET** &nbsp;`api/orgs/{organisationId}/currencies/{currencyId}`

Returns a currency for given id.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-currencies-currencyId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `currencyId` | currency id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CurrencyId` | Currency id. |
| `Code` | Currency code. |
| `Name` | Currency name. |

---

### GetDomesticCurrency

🟢 **GET** &nbsp;`api/orgs/{organisationId}/currencies/date({date})`

Returns a domestic currency.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-currencies-date(date))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `date` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CurrencyId` | Currency id. |
| `Code` | Currency code. |
| `Name` | Currency name. |

---
