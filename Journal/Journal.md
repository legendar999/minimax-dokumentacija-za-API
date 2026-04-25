# Journal

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Journal](https://moj.minimax.si/SI/API/Home/ModuleDetails/Journal)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddJournal](#addjournal) | Adds a new journal. |
| 2 | 🔵 `POST` | [AddVATEntry](#addvatentry) | Adds a VAT entry to a specified journal. |
| 3 | 🔴 `DELETE` | [DeleteJournal](#deletejournal) | Deletes a journal. |
| 4 | 🔴 `DELETE` | [DeleteVATEntry](#deletevatentry) | Deletes a VAT entry. |
| 5 | 🟢 `GET` | [GetJournal](#getjournal) | Returns a journal. |
| 6 | 🟢 `GET` | [GetJournalEntries](#getjournalentries) | Returns all journal entries for a given organisation. |
| 7 | 🟢 `GET` | [GetJournals](#getjournals) | Returns all journals for given organisation. |
| 8 | 🟢 `GET` | [GetJournalsInVODStandard](#getjournalsinvodstandard) | Returns all journals for a given organisation where VODStandardCode exists if issued invoice bookkepping is set to VOD s |
| 9 | 🟢 `GET` | [GetJournalsSyncCandidates](#getjournalssynccandidates) | Returns journals for sync. |
| 10 | 🟢 `GET` | [GetVATEntry](#getvatentry) | Returns a VAT entry. |
| 11 | 🟡 `PUT` | [UpdateJournal](#updatejournal) | Updates journal. |
| 12 | 🟡 `PUT` | [UpdateVATEntry](#updatevatentry) | Updates VAT entry. |

## Kazalo metod

- 🔵 [AddJournal](#addjournal)
- 🔵 [AddVATEntry](#addvatentry)
- 🔴 [DeleteJournal](#deletejournal)
- 🔴 [DeleteVATEntry](#deletevatentry)
- 🟢 [GetJournal](#getjournal)
- 🟢 [GetJournalEntries](#getjournalentries)
- 🟢 [GetJournals](#getjournals)
- 🟢 [GetJournalsInVODStandard](#getjournalsinvodstandard)
- 🟢 [GetJournalsSyncCandidates](#getjournalssynccandidates)
- 🟢 [GetVATEntry](#getvatentry)
- 🟡 [UpdateJournal](#updatejournal)
- 🟡 [UpdateVATEntry](#updatevatentry)

---

## Podrobnosti metod

### AddJournal

🔵 **POST** &nbsp;`api/orgs/{organisationId}/journals`

Adds a new journal.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-journals)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journal` | journal id |

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

### AddVATEntry

🔵 **POST** &nbsp;`api/orgs/{organisationId}/journals/{journalId}/vat`

Adds a VAT entry to a specified journal.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-journals-journalId-vat)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |
| `vatRecord` | vat data |

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

### DeleteJournal

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/journals/{journalId}`

Deletes a journal.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-journals-journalId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |

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

### DeleteVATEntry

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/journals/{journalId}/vat/{vatId}`

Deletes a VAT entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-journals-journalId-vat-vatId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |
| `vatId` | VAT entry id |

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

### GetJournal

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journals/{journalId}`

Returns a journal.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journals-journalId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `JournalId` | Journal id. |
| `JournalType` | class JournalType. Journal type. |
| `JournalDate` | Journal date. |
| `Description` | Journal description. |
| `Status` | Journal status:   O - Draft P - Confirmed A - Automatic  Readonly. |
| `JournalEntries` | Journal entries. List of JournalEntry. |
| `VatEntries` | Vat entries. List of VATEntry. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetJournalEntries

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journals/journal-entries`

Returns all journal entries for a given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journals-journal-entries)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `JournalType` | Journal type. |
| `Description` | Journal description. |
| `AnalyticID` | Analytic id. |
| `CustomerID` | Customer id. |
| `EmployeeId` | Employee id. |
| `Status` | Journal status |
| `Currency` | Currency |
| `DateTo` | Date to. |
| `DateFrom` | Date from. |
| `Account` | Account |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of JournalEntries. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetJournals

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journals`

Returns all journals for given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journals)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `DateTo` | Date to. |
| `DateFrom` | Date from. |
| `JournalId` | JournalId from. |
| `JournalType` | Journal type. |
| `Description` | Journal description. |
| `Status` | Journal status:   O - Draft P - Confirmed A - Automatic |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of JournalSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetJournalsInVODStandard

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journals/vodstandard`

Returns all journals for a given organisation where VODStandardCode exists if issued invoice bookkepping is set to VOD standard.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journals-vodstandard)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `DateTo` | Date to. |
| `DateFrom` | Date from. |
| `JournalId` | JournalId. |
| `FromJournalId` | JournalId from. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

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

### GetJournalsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journals/synccandidates`

Returns journals for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journals-synccandidates)

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

### GetVATEntry

🟢 **GET** &nbsp;`api/orgs/{organisationId}/journals/{journalId}/vat/{vatId}`

Returns a VAT entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-journals-journalId-vat-vatId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |
| `vatId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `VatEntryId` | VAT entry id. |
| `Journal` | class Journal. Journal. |
| `VatDate` | VAT date. |
| `VatBook` | Possible values: (IR, PR). VAT book:   PR - Received invoices book, IR - Issued invoices book |
| `VatAccountingType` | VAT accounting type. |
| `VatEntryDate` | VAT entry date. |
| `Customer` | class Customer. Customer. |
| `Document` | Document. |
| `DocumentDate` | Document date. |
| `ReceivedDate` | Received date. |
| `PaymentDate` | Payment date. |
| `TransactionDate` | Transaction date. |
| `SelfTaxing` | Self-taxing:   D – yes, N – no. |
| `JournalEntry` | class JournalEntry. Journal entry. |
| `JournalEntryExternalId` | Journal entry external ID. |
| `Notes` | Notes. |
| `AdvancePayment` | Advance payment:   D – yes, N – no. |
| `ReportingType` | Reporting Type:   Obracun - (1) regular VAT report Samoprijava - (2) VAT correction or self report SamoprijavaObresti - (3) interests from VAT correction or self report |
| `Analytic` | class Analytic. Analytic. |
| `VatEntryRows` | VAT entry rows. List of VATEntryRow. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### UpdateJournal

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/journals/{journalId}`

Updates journal.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-journals-journalId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |
| `journal` | New journal data. |

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

### UpdateVATEntry

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/journals/{journalId}/vat/{vatId}`

Updates VAT entry.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-journals-journalId-vat-vatId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `journalId` | journal id |
| `vatId` | VAT record id |
| `vatRecord` | VAT data. |

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
