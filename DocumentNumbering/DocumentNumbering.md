# DocumentNumbering

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/DocumentNumbering](https://moj.minimax.si/SI/API/Home/ModuleDetails/DocumentNumbering)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetDocumentNumbering](#getdocumentnumbering) | Returns a document numbering for given id. |
| 2 | 🟢 `GET` | [GetDocumentNumberings](#getdocumentnumberings) | Returns DocumentNumbering for issued and proforma invoices. |

## Kazalo metod

- 🟢 [GetDocumentNumbering](#getdocumentnumbering)
- 🟢 [GetDocumentNumberings](#getdocumentnumberings)

---

## Podrobnosti metod

### GetDocumentNumbering

🟢 **GET** &nbsp;`api/orgs/{organisationId}/document-numbering/{documentNumberingId}`

Returns a document numbering for given id.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-document-numbering-documentNumberingId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentNumberingId` | document id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `DocumentNumberingId` | DocumentNumbering id. |
| `Document` | Possible values: (IR, PD, PR). Document numbering codes.  IR – Issued invoice PD – Proforma invoice PR – Received invoice |
| `Code` | Code. |
| `Name` | Name. |
| `Default` | Possible values: (D, N). Default:
   D - Yes N - No |
| `ReferenceNumber` | Reference number used on invoices. |
| `Usage` | Possible values: (D, N). Usage:
   D - Yes N - No |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetDocumentNumberings

🟢 **GET** &nbsp;`api/orgs/{organisationId}/document-numbering`

Returns DocumentNumbering for issued and proforma invoices.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-document-numbering)

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
| `Rows` | Returned rows. List of DocumentNumbering. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
