# Document

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Document](https://moj.minimax.si/SI/API/Home/ModuleDetails/Document)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddDocument](#adddocument) | Adds a new document. |
| 2 | 🔵 `POST` | [AddDocumentAttachment](#adddocumentattachment) | Adds a new document attachment. |
| 3 | 🔴 `DELETE` | [DeleteDocument](#deletedocument) | Deletes document. |
| 4 | 🔴 `DELETE` | [DeleteDocumentAttachment](#deletedocumentattachment) | Deletes document attachment. |
| 5 | 🟢 `GET` | [GetDocument](#getdocument) | Returns a document. |
| 6 | 🟢 `GET` | [GetDocumentAttachment](#getdocumentattachment) | Returns a document attachment. |
| 7 | 🟢 `GET` | [GetDocuments](#getdocuments) | Returns all documents for the given organization. |
| 8 | 🟢 `GET` | [GetDocumentsSyncCandidates](#getdocumentssynccandidates) | Returns documents for sync. |
| 9 | 🟡 `PUT` | [UpdateDocument](#updatedocument) | Updates document. |
| 10 | 🟡 `PUT` | [UpdateDocumentAttachment](#updatedocumentattachment) | Updates document attachment. |

## Kazalo metod

- 🔵 [AddDocument](#adddocument)
- 🔵 [AddDocumentAttachment](#adddocumentattachment)
- 🔴 [DeleteDocument](#deletedocument)
- 🔴 [DeleteDocumentAttachment](#deletedocumentattachment)
- 🟢 [GetDocument](#getdocument)
- 🟢 [GetDocumentAttachment](#getdocumentattachment)
- 🟢 [GetDocuments](#getdocuments)
- 🟢 [GetDocumentsSyncCandidates](#getdocumentssynccandidates)
- 🟡 [UpdateDocument](#updatedocument)
- 🟡 [UpdateDocumentAttachment](#updatedocumentattachment)

---

## Podrobnosti metod

### AddDocument

🔵 **POST** &nbsp;`api/orgs/{organisationId}/documents`

Adds a new document.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-documents)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `document` | document |

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

### AddDocumentAttachment

🔵 **POST** &nbsp;`api/orgs/{organisationId}/documents/{documentId}/attachments`

Adds a new document attachment.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-documents-documentId-attachments)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |
| `documentAttachment` | document attachment |

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

### DeleteDocument

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/documents/{documentId}`

Deletes document.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-documents-documentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |

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

### DeleteDocumentAttachment

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/documents/{documentId}/attachments/{documentAttachmentId}`

Deletes document attachment.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-documents-documentId-attachments-documentAttachmentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |
| `documentAttachmentId` | document attachment id |

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

### GetDocument

🟢 **GET** &nbsp;`api/orgs/{organisationId}/documents/{documentId}`

Returns a document.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-documents-documentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `DocumentId` | Document id. |
| `DocumentDate` | Document date. |
| `Customer` | class Customer. Customer. |
| `Employee` | class Employee. Employee. |
| `Description` | Document description. |
| `Attachments` | Document attachments. List of AttachmentLink. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetDocumentAttachment

🟢 **GET** &nbsp;`api/orgs/{organisationId}/documents/{documentId}/attachments/{documentAttachmentId}`

Returns a document attachment.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-documents-documentId-attachments-documentAttachmentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |
| `documentAttachmentId` | document attachment id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `DocumentAttachmentId` | Document attachment id. |
| `Document` | class Document. Document. |
| `Description` | Attachment description. |
| `AttachmentData` | Attachment data. |
| `FileName` | Attachment name for file. |
| `MimeType` | Attachment mime type. |
| `EntryDate` | Entry date. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetDocuments

🟢 **GET** &nbsp;`api/orgs/{organisationId}/documents`

Returns all documents for the given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-documents)

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
| `Rows` | Returned rows. List of DocumentSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetDocumentsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/documents/synccandidates`

Returns documents for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-documents-synccandidates)

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

### UpdateDocument

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/documents/{documentId}`

Updates document.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-documents-documentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |
| `document` | New document data. |

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

### UpdateDocumentAttachment

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/documents/{documentId}/attachments/{documentAttachmentId}`

Updates document attachment.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-documents-documentId-attachments-documentAttachmentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `documentId` | document id |
| `documentAttachmentId` | document attachment id |
| `documentAttachment` | New documentAttachment data. |

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
