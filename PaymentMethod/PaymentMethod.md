# PaymentMethod

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/PaymentMethod](https://moj.minimax.si/SI/API/Home/ModuleDetails/PaymentMethod)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetPaymentMethods](#getpaymentmethods) | Returns all payment methods for given organisation. |

## Kazalo metod

- 🟢 [GetPaymentMethods](#getpaymentmethods)

---

## Podrobnosti metod

### GetPaymentMethods

🟢 **GET** &nbsp;`api/orgs/{organisationId}/paymentMethods`

Returns all payment methods for given organisation.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-paymentMethods)

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
| `Rows` | Returned rows. List of PaymentMethodSearch. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
