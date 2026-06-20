# Outbox

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Outbox](https://moj.minimax.si/SI/API/Home/ModuleDetails/Outbox)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetOutboxItem](#getoutboxitem) | Returns the specified outbox item. |
| 2 | 🟢 `GET` | [GetOutboxItems](#getoutboxitems) | Returns all outbox Items for a given organization. |

## Kazalo metod

- 🟢 [GetOutboxItem](#getoutboxitem)
- 🟢 [GetOutboxItems](#getoutboxitems)

---

## Podrobnosti metod

### GetOutboxItem

🟢 **GET** &nbsp;`api/orgs/{organisationId}/outbox/{outboxId}`

Returns the specified outbox item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-outbox-outboxId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `outboxId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `OutboxId` |  |
| `Customer` | class Customer. Customer. |
| `Employee` | class Employee. Employee. |
| `OutboxDate` | Outbox date. |
| `OutboxType` | Outbox type:
   IR - Issued invoices DO - Delivery note OP - Payroll |
| `Description` | Description |
| `Attachments` | Outbox attachments. List of OutboxAttachment. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetOutboxItems

🟢 **GET** &nbsp;`api/orgs/{organisationId}/outbox`

Returns all outbox Items for a given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-outbox)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `OutboxType` | Outbox type. |
| `OutboxImportStatus` | Outbox import status |
| `OutboxDateFrom` | Outbox date from. |
| `OutboxDateTo` | Outbox date to. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of Outbox. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
