# Account

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Account](https://moj.minimax.si/SI/API/Home/ModuleDetails/Account)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetAccount](#getaccount) | Returns an account. |
| 2 | 🟢 `GET` | [GetAccountByCode](#getaccountbycode) | Returns an account for its code. |
| 3 | 🟢 `GET` | [GetAccountByContent](#getaccountbycontent) | Returns an account for the corresponding content (based on Organization settings). |
| 4 | 🟢 `GET` | [GetAccounts](#getaccounts) | Returns all accounts for given organisation. |
| 5 | 🟢 `GET` | [GetAccountsSyncCandidates](#getaccountssynccandidates) | Returns accounts for sync. |

## Kazalo metod

- 🟢 [GetAccount](#getaccount)
- 🟢 [GetAccountByCode](#getaccountbycode)
- 🟢 [GetAccountByContent](#getaccountbycontent)
- 🟢 [GetAccounts](#getaccounts)
- 🟢 [GetAccountsSyncCandidates](#getaccountssynccandidates)

---

## Podrobnosti metod

### GetAccount

🟢 **GET** &nbsp;`api/orgs/{organisationId}/accounts/{accountId}`

Returns an account.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-accounts-accountId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `accountId` | account id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `AccountId` | Account id. |
| `Code` | Account code. |
| `Name` | Account name. |
| `NameInOtherLanguage` | Other language account name. |
| `NameInEnglish` | English account name. |
| `Description` | Account description. |
| `AllowedPosting` | Possible values: (V, B, D, N). Posting side:    V – debit and credit, B – only debit, D – only credit, N – Posting is not allowed. |
| `InvoiceAccounting` | Possible values: (N, B, D). Account posting:    N – No account, B – debit D – credit |
| `AnalyticsEntry` | Possible values: (V, N, D). Analytics entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `EmployeeEntry` | Employee entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `CustomerEntry` | Possible values: (V, N, D). Customer entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `NonTaxable` | Possible values: (D, N). Unrecognized account in terms of tax:   N – No, D – Yes. |
| `Application` | Possible values: (D, N). Application:   N – No, D – Yes. |
| `ValidFromYear` | Account validity from year. Readonly. |
| `ValidToYear` | Account validity to year. Readonly. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetAccountByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/accounts/code({code})`

Returns an account for its code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-accounts-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `code` | Account code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `AccountId` | Account id. |
| `Code` | Account code. |
| `Name` | Account name. |
| `NameInOtherLanguage` | Other language account name. |
| `NameInEnglish` | English account name. |
| `Description` | Account description. |
| `AllowedPosting` | Possible values: (V, B, D, N). Posting side:    V – debit and credit, B – only debit, D – only credit, N – Posting is not allowed. |
| `InvoiceAccounting` | Possible values: (N, B, D). Account posting:    N – No account, B – debit D – credit |
| `AnalyticsEntry` | Possible values: (V, N, D). Analytics entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `EmployeeEntry` | Employee entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `CustomerEntry` | Possible values: (V, N, D). Customer entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `NonTaxable` | Possible values: (D, N). Unrecognized account in terms of tax:   N – No, D – Yes. |
| `Application` | Possible values: (D, N). Application:   N – No, D – Yes. |
| `ValidFromYear` | Account validity from year. Readonly. |
| `ValidToYear` | Account validity to year. Readonly. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetAccountByContent

🟢 **GET** &nbsp;`api/orgs/{organisationId}/accounts/content({content})`

Returns an account for the corresponding content (based on Organization settings).

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-accounts-content(content))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `content` | Describes an Account by its content. Supported values:  OtherRevenues,  FinancialRevenue,  RevenueFromSellingGoodsInHomeCountry,  RevenueFromSellingGoodsInEU,  RevenueFromSellingGoodsInThirdCountries,  RevenueFromSellingProductsInHomeCountry,  RevenueFromSellingProductsInEU,  RevenueFromSellingProductsInThirdCountries,  RevenueFromSellingMaterialsInHomeCountry,  RevenueFromSellingMaterialsInEU,  RevenueFromSellingMaterialsInThirdCountries,  RevenueFromSellingServicesInHomeCountry,  RevenueFromSellingServicesInEU,  RevenueFromSellingServicesInThirdCountries,  RevenueFromExchangeRateDifferences |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `AccountId` | Account id. |
| `Code` | Account code. |
| `Name` | Account name. |
| `NameInOtherLanguage` | Other language account name. |
| `NameInEnglish` | English account name. |
| `Description` | Account description. |
| `AllowedPosting` | Possible values: (V, B, D, N). Posting side:    V – debit and credit, B – only debit, D – only credit, N – Posting is not allowed. |
| `InvoiceAccounting` | Possible values: (N, B, D). Account posting:    N – No account, B – debit D – credit |
| `AnalyticsEntry` | Possible values: (V, N, D). Analytics entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `EmployeeEntry` | Employee entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `CustomerEntry` | Possible values: (V, N, D). Customer entry:   V – Input allowed, N – Input not allowed, D – Mandatory input. |
| `NonTaxable` | Possible values: (D, N). Unrecognized account in terms of tax:   N – No, D – Yes. |
| `Application` | Possible values: (D, N). Application:   N – No, D – Yes. |
| `ValidFromYear` | Account validity from year. Readonly. |
| `ValidToYear` | Account validity to year. Readonly. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetAccounts

🟢 **GET** &nbsp;`api/orgs/{organisationId}/accounts`

Returns all accounts for given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-accounts)

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
| `Rows` | Returned rows. List of Account. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetAccountsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/accounts/synccandidates`

Returns accounts for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-accounts-synccandidates)

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
