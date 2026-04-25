# Employee

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Employee](https://moj.minimax.si/SI/API/Home/ModuleDetails/Employee)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddEmployee](#addemployee) | Adds a new employee. |
| 2 | 🔴 `DELETE` | [DeleteEmployee](#deleteemployee) | Deletes employee. |
| 3 | 🟢 `GET` | [GetEmployee](#getemployee) | Returns an employee. |
| 4 | 🟢 `GET` | [GetEmployees](#getemployees) | Returns all employees for the given organization. |
| 5 | 🟢 `GET` | [GetEmployeesSyncCandidates](#getemployeessynccandidates) | Returns employees for sync. |
| 6 | 🟡 `PUT` | [UpdateEmployee](#updateemployee) | Updates employee. |

## Kazalo metod

- 🔵 [AddEmployee](#addemployee)
- 🔴 [DeleteEmployee](#deleteemployee)
- 🟢 [GetEmployee](#getemployee)
- 🟢 [GetEmployees](#getemployees)
- 🟢 [GetEmployeesSyncCandidates](#getemployeessynccandidates)
- 🟡 [UpdateEmployee](#updateemployee)

---

## Podrobnosti metod

### AddEmployee

🔵 **POST** &nbsp;`api/orgs/{organisationId}/employees`

Adds a new employee.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-employees)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `employee` | employee |

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

### DeleteEmployee

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/employees/{employeeId}`

Deletes employee.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-employees-employeeId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `employeeId` | employee id |

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

### GetEmployee

🟢 **GET** &nbsp;`api/orgs/{organisationId}/employees/{employeeId}`

Returns an employee.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-employees-employeeId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `employeeId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `EmployeeId` | Employee id. |
| `Code` | Employee code. |
| `TaxNumber` | Employee Tax number. |
| `FirstName` | Employee first name. |
| `LastName` | Employee last name. |
| `Address` | Employee address. |
| `PostalCode` | Employee postal code. |
| `City` | Employee city. |
| `Country` | class Country. Employee country. |
| `CountryOfResidence` | class Country. Employee residence country. |
| `DateOfBirth` | Employee date of birth. |
| `Gender` | Possible values: (M, Z). Employee gender:   M - Man Z - Woman |
| `EmploymentStartDate` | Date of employment. |
| `EmploymentEndDate` | Employment end date. |
| `Notes` | Notes. |
| `EmploymentType` | Employment type:   ZD - Employed worker ZL - Employed owner ZAP - Employed elsewhere DSP - Pupil or student on compulsory practical training DD - Seconded worker ZJD - Employee - community work |
| `PersonalIdenficationNumber` | Employee Personal identification number. |
| `InsuranceBasis` | Employee Insurance base for employment type ZL and organisation type »Zasebnik«:   005 - Basis 005   EmploymentType ZL and organisation type »Gospodarska družba«:   040in112 - Basis 040 + 112, 040 - Basis 040, 103 - Basis 103. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetEmployees

🟢 **GET** &nbsp;`api/orgs/{organisationId}/employees`

Returns all employees for the given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-employees)

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
| `Rows` | Returned rows. List of EmployeeSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetEmployeesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/employees/synccandidates`

Returns employees for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-employees-synccandidates)

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

### UpdateEmployee

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/employees/{employeeId}`

Updates employee.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-employees-employeeId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `employeeId` | employee id |
| `employee` | New employee data. |

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
