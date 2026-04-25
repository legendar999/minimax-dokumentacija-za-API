# Customer

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Customer](https://moj.minimax.si/SI/API/Home/ModuleDetails/Customer)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddCustomer](#addcustomer) | Adds a new customer. |
| 2 | 🔵 `POST` | [AddCustomerByTaxNumber](#addcustomerbytaxnumber) | Adds a new customer according to the tax number. |
| 3 | 🔴 `DELETE` | [DeleteCustomer](#deletecustomer) | Deletes customer. |
| 4 | 🟢 `GET` | [GetCustomer](#getcustomer) | Returns a customer. |
| 5 | 🟢 `GET` | [GetCustomerByCode](#getcustomerbycode) | Returns a customer with given code. |
| 6 | 🟢 `GET` | [GetCustomers](#getcustomers) | Returns all customers for given organisation. |
| 7 | 🟢 `GET` | [GetCustomersSyncCandidates](#getcustomerssynccandidates) | Returns customers that match filter criteria for sync. |
| 8 | 🟡 `PUT` | [UpdateCustomer](#updatecustomer) | Updates customer. |

## Kazalo metod

- 🔵 [AddCustomer](#addcustomer)
- 🔵 [AddCustomerByTaxNumber](#addcustomerbytaxnumber)
- 🔴 [DeleteCustomer](#deletecustomer)
- 🟢 [GetCustomer](#getcustomer)
- 🟢 [GetCustomerByCode](#getcustomerbycode)
- 🟢 [GetCustomers](#getcustomers)
- 🟢 [GetCustomersSyncCandidates](#getcustomerssynccandidates)
- 🟡 [UpdateCustomer](#updatecustomer)

---

## Podrobnosti metod

### AddCustomer

🔵 **POST** &nbsp;`api/orgs/{organisationId}/customers`

Adds a new customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-customers)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customer` | customer id |

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

### AddCustomerByTaxNumber

🔵 **POST** &nbsp;`api/orgs/{organisationId}/customers/addbytaxnumber({taxNumber})`

Adds a new customer according to the tax number.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-customers-addbytaxnumber(taxNumber))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `taxNumber` |  |

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

### DeleteCustomer

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/customers/{customerId}`

Deletes customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-customers-customerId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |

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

### GetCustomer

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}`

Returns a customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CustomerId` | Customer id. |
| `Code` | Customer code, unique within organisation. |
| `Name` | Customer name. |
| `Address` | Customer address. |
| `PostalCode` | Customer postal code. |
| `City` | Customer city. |
| `Country` | class Country. Customer country. |
| `CountryName` | Country name. |
| `TaxNumber` | Customer tax number. |
| `RegistrationNumber` | Customer registration number. |
| `VATIdentificationNumber` | Customer VAT Identification Number. |
| `SubjectToVAT` | Possible values: (D, M, N). Customer VAT settings.  For EU customers:   D - Legal person or a person with business who is subject to VAT, M - Legal person or a person with business who is NOT subject to VAT, N – Enduser.   For customers outside EU:   D - Legal person (VAT on the issued invoice is not to be accounted for), N – Enduser. |
| `ConsiderCountryForBookkeeping` | Possible values: (D, N). Take customers country into account for bookkeeping (Foreign endusers only).  Usage:   D - Yes, N - No. |
| `Currency` | class Currency. Default currency. |
| `ExpirationDays` | Invoice expiration days. |
| `RebatePercent` | Rebate (%) |
| `WebSiteURL` | Web site. |
| `EInvoiceIssuing` | Possible values: (SeNePripravlja, RocniIzvoz, Ponudnik, EPosta). e-Invoices issuing type:    SeNePripravlja - None(won't be prepared) RocniIzvoz - Import to bank Ponudnik -Import to ZZInet EPosta - Send by email |
| `InternalCustomerNumber` | Internal reference for e-invoices. |
| `GLN` | GLN |
| `BudgetUserNumber` |  |
| `Usage` | Possible values: (D, N). Usage:   D - Yes, N - No. |
| `AssociationType` | Possible values: (Maticna, Odvisna, Ostala). |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetCustomerByCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/code({code})`

Returns a customer with given code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-code(code))

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `code` | customer code |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `CustomerId` | Customer id. |
| `Code` | Customer code, unique within organisation. |
| `Name` | Customer name. |
| `Address` | Customer address. |
| `PostalCode` | Customer postal code. |
| `City` | Customer city. |
| `Country` | class Country. Customer country. |
| `CountryName` | Country name. |
| `TaxNumber` | Customer tax number. |
| `RegistrationNumber` | Customer registration number. |
| `VATIdentificationNumber` | Customer VAT Identification Number. |
| `SubjectToVAT` | Possible values: (D, M, N). Customer VAT settings.  For EU customers:   D - Legal person or a person with business who is subject to VAT, M - Legal person or a person with business who is NOT subject to VAT, N – Enduser.   For customers outside EU:   D - Legal person (VAT on the issued invoice is not to be accounted for), N – Enduser. |
| `ConsiderCountryForBookkeeping` | Possible values: (D, N). Take customers country into account for bookkeeping (Foreign endusers only).  Usage:   D - Yes, N - No. |
| `Currency` | class Currency. Default currency. |
| `ExpirationDays` | Invoice expiration days. |
| `RebatePercent` | Rebate (%) |
| `WebSiteURL` | Web site. |
| `EInvoiceIssuing` | Possible values: (SeNePripravlja, RocniIzvoz, Ponudnik, EPosta). e-Invoices issuing type:    SeNePripravlja - None(won't be prepared) RocniIzvoz - Import to bank Ponudnik -Import to ZZInet EPosta - Send by email |
| `InternalCustomerNumber` | Internal reference for e-invoices. |
| `GLN` | GLN |
| `BudgetUserNumber` |  |
| `Usage` | Possible values: (D, N). Usage:   D - Yes, N - No. |
| `AssociationType` | Possible values: (Maticna, Odvisna, Ostala). |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetCustomers

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers`

Returns all customers for given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers)

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
| `Rows` | Returned rows. List of CustomerSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetCustomersSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/synccandidates`

Returns customers that match filter criteria for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-synccandidates)

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

### UpdateCustomer

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/customers/{customerId}`

Updates customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-customers-customerId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `customer` | New customer data. |

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
