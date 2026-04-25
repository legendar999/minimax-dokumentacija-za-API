# Analytic

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Analytic](https://moj.minimax.si/SI/API/Home/ModuleDetails/Analytic)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddAnalytic](#addanalytic) | Adds a new analytic. |
| 2 | 🔴 `DELETE` | [DeleteAnalytic](#deleteanalytic) | Deletes analytic. |
| 3 | 🟢 `GET` | [GetAnalytic](#getanalytic) | Returns an analytic. |
| 4 | 🟢 `GET` | [GetAnalytics](#getanalytics) | Returns all analytics for the given organization. |
| 5 | 🟢 `GET` | [GetAnalyticsSyncCandidates](#getanalyticssynccandidates) | Returns analytics for sync. |
| 6 | 🟡 `PUT` | [UpdateAnalytic](#updateanalytic) | Updates analytic. |

## Kazalo metod

- 🔵 [AddAnalytic](#addanalytic)
- 🔴 [DeleteAnalytic](#deleteanalytic)
- 🟢 [GetAnalytic](#getanalytic)
- 🟢 [GetAnalytics](#getanalytics)
- 🟢 [GetAnalyticsSyncCandidates](#getanalyticssynccandidates)
- 🟡 [UpdateAnalytic](#updateanalytic)

---

## Podrobnosti metod

### AddAnalytic

🔵 **POST** &nbsp;`api/orgs/{organisationId}/analytics`

Adds a new analytic.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-analytics)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `analytic` | analytic |

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

### DeleteAnalytic

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/analytics/{analyticId}`

Deletes analytic.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-analytics-analyticId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `analyticId` | analytic id |

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

### GetAnalytic

🟢 **GET** &nbsp;`api/orgs/{organisationId}/analytics/{analyticId}`

Returns an analytic.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-analytics-analyticId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `analyticId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `AnalyticId` | Analytic id. |
| `Code` | Analytic code. |
| `Name` | Analytic name. |
| `UsageEndDate` | Usage end date. |
| `ParentAnalytic` | class Analytic. Parent analytic. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetAnalytics

🟢 **GET** &nbsp;`api/orgs/{organisationId}/analytics`

Returns all analytics for the given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-analytics)

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
| `Rows` | Returned rows. List of AnalyticSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetAnalyticsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/analytics/synccandidates`

Returns analytics for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-analytics-synccandidates)

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

### UpdateAnalytic

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/analytics/{analyticId}`

Updates analytic.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-analytics-analyticId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `analyticId` | analytic id |
| `analytic` | New analytic data. |

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
