# VatRate

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/VatRate](https://moj.minimax.si/SI/API/Home/ModuleDetails/VatRate)  
> **Generirano:** 25. 04. 2026 ob 12:16  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetVatRateByCode](#getvatratebycode) | Returns a vat rate for its code. |
| 2 | 🟢 `GET` | [GetVatRateByID](#getvatratebyid) | Returns a vat rate for its ID. |
| 3 | 🟢 `GET` | [GetVatRates](#getvatrates) | Returns all vat rates. |
| 4 | 🟢 `GET` | [GetVatRatesSyncCandidates](#getvatratessynccandidates) | Returns vat rates for sync. |

## Kazalo metod

- 🟢 [GetVatRateByCode](#getvatratebycode)
- 🟢 [GetVatRateByID](#getvatratebyid)
- 🟢 [GetVatRates](#getvatrates)
- 🟢 [GetVatRatesSyncCandidates](#getvatratessynccandidates)

---

## Podrobnosti metod

### GetVatRateByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/vatrates/code({code})?date={date}&countryID={countryID}`

Returns a vat rate for its code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-vatrates-code(code)_date_countryID)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation ID |
| `code` | VatRate Code |
| `date` | Date (Format: YYYY-MM-DD) |
| `countryID` | Country ID |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `VatRateId` | Vat rate id. |
| `Code` | VAT rate codes:
   S - Standard rate Z - Reduced rate P - Flat rate 0 - Lower rate O - Exempted N - Non-taxable |
| `Percent` | Interest percent. |
| `VatRatePercentage` | VatRate Percentage. |

---

### GetVatRateByID

🟢 **GET** &nbsp;`api/orgs/{organisationId}/vatrates/{vatRateId}?date={date}&countryID={countryID}`

Returns a vat rate for its ID.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-vatrates-vatRateId_date_countryID)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation ID |
| `vatRateId` | VatRate ID |
| `date` | Date (Format: YYYY-MM-DD) |
| `countryID` | Country |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `VatRateId` | Vat rate id. |
| `Code` | VAT rate codes:
   S - Standard rate Z - Reduced rate P - Flat rate 0 - Lower rate O - Exempted N - Non-taxable |
| `Percent` | Interest percent. |
| `VatRatePercentage` | VatRate Percentage. |

---

### GetVatRates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/vatrates?date={date}&countryID={countryID}`

Returns all vat rates.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-vatrates_date_countryID)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation ID |
| `date` | Date (Format: YYYY-MM-DD) |
| `countryID` | Country ID |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of VatRate. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetVatRatesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/vatrates/synccandidates`

Returns vat rates for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-vatrates-synccandidates)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation ID |
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
