# ReportTemplate

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/ReportTemplate](https://moj.minimax.si/SI/API/Home/ModuleDetails/ReportTemplate)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetReportTemplate](#getreporttemplate) | Returns a report template. |
| 2 | 🟢 `GET` | [GetReportTemplates](#getreporttemplates) | Returns all report templates. |
| 3 | 🟢 `GET` | [GetReportTemplateSyncCandidates](#getreporttemplatesynccandidates) | Returns report templates for sync. |

## Kazalo metod

- 🟢 [GetReportTemplate](#getreporttemplate)
- 🟢 [GetReportTemplates](#getreporttemplates)
- 🟢 [GetReportTemplateSyncCandidates](#getreporttemplatesynccandidates)

---

## Podrobnosti metod

### GetReportTemplate

🟢 **GET** &nbsp;`api/orgs/{organisationId}/report-templates/{reportTemplateId}`

Returns a report template.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-report-templates-reportTemplateId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `reportTemplateId` | Report template id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `ReportTemplateId` | Report template id. |
| `Name` | Report template name. |
| `DisplayType` | Report template display type:
   BB - Gross balance BK - Compensation DN - Work order DO - Delivery note DOP - Calculation sheet DP – credit note IN – Issued order IO – Open items report IR – Issued invoice OP - Payment reminder PL - Salaries, payslips PN – Received order confirmation PUPN – proforma invoice with order for payment UP - Issued invoice with order for payment ZO - Interest for delay. |
| `Default` | Default report template:
   D - Yes, N - No. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetReportTemplates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/report-templates`

Returns all report templates.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-report-templates)

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
| `Rows` | Returned rows. List of ReportTemplate. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetReportTemplateSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/report-templates/synccandidates`

Returns report templates for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-report-templates-synccandidates)

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
