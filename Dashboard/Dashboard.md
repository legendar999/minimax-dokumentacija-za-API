# Dashboard

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Dashboard](https://moj.minimax.si/SI/API/Home/ModuleDetails/Dashboard)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetDashboards](#getdashboards) | Returns dashboards data. |

## Kazalo metod

- 🟢 [GetDashboards](#getdashboards)

---

## Podrobnosti metod

### GetDashboards

🟢 **GET** &nbsp;`api/orgs/{organisationId}/dashboards`

Returns dashboards data.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-dashboards)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `IssuedInvoicesSummary` |  |
| `ReceivedInvoicesSummary` |  |
| `IssuedInvoicesUnpaid` |  |
| `ReceivedInvoicesUnpaid` |  |
| `TopCustomers` |  |
| `TopDebtors` |  |
| `TopSuppliers` |  |
| `TopCreditors` |  |
| `RevenuesExpenses` |  |

---
