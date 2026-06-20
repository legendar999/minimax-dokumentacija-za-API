# Inbox

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Inbox](https://moj.minimax.si/SI/API/Home/ModuleDetails/Inbox)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddInboxAttachments](#addinboxattachments) | Adds the specified inbox attachements to the inbox. |
| 2 | 🔵 `POST` | [AddInboxItem](#addinboxitem) | Adds the specified item to the inbox. |
| 3 | 🟡 `PUT` | [CustomActionInbox](#customactioninbox) | Performs a custom action on inbox.
 Available actionName values: 
approve
reject


Other parameters:
 
rejectionReason |
| 4 | 🔴 `DELETE` | [DeleteInboxAttachment](#deleteinboxattachment) | Deletes the specified attachment from the inbox item. |
| 5 | 🔴 `DELETE` | [DeleteInboxItem](#deleteinboxitem) | Deletes the specified item from the inbox. |
| 6 | 🟢 `GET` | [GetInboxItem](#getinboxitem) | Returns the specified inbox item. |
| 7 | 🟢 `GET` | [GetInboxItems](#getinboxitems) | Returns all inbox Items for a given organization. |

## Kazalo metod

- 🔵 [AddInboxAttachments](#addinboxattachments)
- 🔵 [AddInboxItem](#addinboxitem)
- 🟡 [CustomActionInbox](#customactioninbox)
- 🔴 [DeleteInboxAttachment](#deleteinboxattachment)
- 🔴 [DeleteInboxItem](#deleteinboxitem)
- 🟢 [GetInboxItem](#getinboxitem)
- 🟢 [GetInboxItems](#getinboxitems)

---

## Podrobnosti metod

### AddInboxAttachments

🔵 **POST** &nbsp;`api/orgs/{organisationId}/inbox/{inboxId}`

Adds the specified inbox attachements to the inbox.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-inbox-inboxId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `inboxId` |  |
| `attachements` |  |

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

### AddInboxItem

🔵 **POST** &nbsp;`api/orgs/{organisationId}/inbox`

Adds the specified item to the inbox.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-inbox)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `inbox` |  |

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

### CustomActionInbox

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/inbox/{inboxId}/actions/{actionName}`

Performs a custom action on inbox.
 Available actionName values: 
approve
reject


Other parameters:
 
rejectionReason: used with the reject action.
approvalReason: used with the approve action.
createReceivedInvoice

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-inbox-inboxId-actions-actionName)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | Organisation id |
| `inboxId` | InboxId id |
| `actionName` | Available actionName values: {"approve", "reject"} |

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

### DeleteInboxAttachment

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/inbox/{inboxId}/attachments/{inboxAttachmentId}`

Deletes the specified attachment from the inbox item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-inbox-inboxId-attachments-inboxAttachmentId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `inboxId` |  |
| `inboxAttachmentId` |  |

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

### DeleteInboxItem

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/inbox/{inboxId}`

Deletes the specified item from the inbox.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-inbox-inboxId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `inboxId` |  |

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

### GetInboxItem

🟢 **GET** &nbsp;`api/orgs/{organisationId}/inbox/{inboxId}`

Returns the specified inbox item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-inbox-inboxId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `inboxId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `InboxId` |  |
| `Customer` | class Customer. Customer. |
| `Employee` | class Employee. Employee. |
| `InboxDate` | Inbox date. |
| `InboxType` | Inbox type:
   PR - for received invoice IZP - for bank statements Ostalo - for other types Neznano - for unknown types |
| `Description` | Description |
| `StatusOfReceivedInvoice` | Status of recived invoice:
   Zavrnjen – Rejected Storniran – Revoked Odobren – Approved Preklican – Canceled   Readonly. |
| `BookkeepingAllowed` | Defines if received invoice has allowed bookkepping even though it is not Approved. Readonly. |
| `EProvider` | Provider of the electronic route. Readonly. |
| `Attachments` | Inbox attachments. List of InboxAttachment. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetInboxItems

🟢 **GET** &nbsp;`api/orgs/{organisationId}/inbox`

Returns all inbox Items for a given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-inbox)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `InboxType` | Inbox type. |
| `InboxImportStatus` | Inbox import status |
| `InboxDateFrom` | Inbox date from. |
| `InboxDateTo` | Inbox date to. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of Inbox. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
