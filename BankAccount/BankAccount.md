# BankAccount

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/BankAccount](https://moj.minimax.si/SI/API/Home/ModuleDetails/BankAccount)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddBankAccount](#addbankaccount) | Adds a new bank account to a specified customer. |
| 2 | 🔴 `DELETE` | [DeleteBankAccount](#deletebankaccount) | Deletes a bank account. |
| 3 | 🟢 `GET` | [GetBankAccount](#getbankaccount) | Returns a bank account. |
| 4 | 🟢 `GET` | [GetBankAccounts](#getbankaccounts) | Returns all bank accounts for a given customer. |
| 5 | 🟢 `GET` | [GetBankAccountsSyncCandidates](#getbankaccountssynccandidates) | Returns bank accounts for sync. |
| 6 | 🟡 `PUT` | [UpdateBankAccount](#updatebankaccount) | Updates a bank account. |

## Kazalo metod

- 🔵 [AddBankAccount](#addbankaccount)
- 🔴 [DeleteBankAccount](#deletebankaccount)
- 🟢 [GetBankAccount](#getbankaccount)
- 🟢 [GetBankAccounts](#getbankaccounts)
- 🟢 [GetBankAccountsSyncCandidates](#getbankaccountssynccandidates)
- 🟡 [UpdateBankAccount](#updatebankaccount)

---

## Podrobnosti metod

### AddBankAccount

🔵 **POST** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/bankAccounts`

Adds a new bank account to a specified customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-customers-customerId-bankAccounts)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `account` | account data |

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

### DeleteBankAccount

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/bankAccounts/{bankAccountId}`

Deletes a bank account.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-customers-customerId-bankAccounts-bankAccountId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `bankAccountId` | account id |

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

### GetBankAccount

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/bankAccounts/{bankAccountId}`

Returns a bank account.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-bankAccounts-bankAccountId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `bankAccountId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `BankAccountId` | Bank account id. |
| `Customer` | class Customer. Customer. |
| `Name` | Bank account name. |
| `IBAN` | IBAN: Country code and check digits. |
| `AccountNumber` | Basic Bank Account Number. |
| `BIC` | Bank Identifier Code. |
| `Default` | Default IBAN:   D – Yes, N – No. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetBankAccounts

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/bankAccounts`

Returns all bank accounts for a given customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-bankAccounts)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of BankAccount. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetBankAccountsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/bankAccounts/synccandidates`

Returns bank accounts for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-bankAccounts-synccandidates)

---

### UpdateBankAccount

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/bankAccounts/{bankAccountId}`

Updates a bank account.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-customers-customerId-bankAccounts-bankAccountId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `bankAccountId` | bank account id |
| `account` | account data |

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
