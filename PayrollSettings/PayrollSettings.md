# PayrollSettings

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/PayrollSettings](https://moj.minimax.si/SI/API/Home/ModuleDetails/PayrollSettings)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetPayrollSettingByCodeAndDate](#getpayrollsettingbycodeanddate) | Returns payroll settings for given code, customer code and date (YYYYMMDD). |

## Kazalo metod

- 🟢 [GetPayrollSettingByCodeAndDate](#getpayrollsettingbycodeanddate)

---

## Podrobnosti metod

### GetPayrollSettingByCodeAndDate

🟢 **GET** &nbsp;`api/payrollsettings/{payrollSettingCode}?externalUserIdentifier={externalUserIdentifier}&customerCode={customerCode}&date={date}`

Returns payroll settings for given code, customer code and date (YYYYMMDD).

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-payrollsettings-payrollSettingCode_externalUserIdentifier_customerCode_date)

#### Request parametri

| Property | Description |
| --- | --- |
| `payrollSettingCode` |  |
| `externalUserIdentifier` |  |
| `customerCode` |  |
| `date` |  |
| `SearchString` | Search string. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of PayrollSettings. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
