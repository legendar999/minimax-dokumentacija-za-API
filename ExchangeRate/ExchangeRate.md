# ExchangeRate

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/ExchangeRate](https://moj.minimax.si/SI/API/Home/ModuleDetails/ExchangeRate)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetExchangeRateByCurrencyCode](#getexchangeratebycurrencycode) | Returns the daily exchange rate for the currency that corresponds with the specified code. |
| 2 | 🟢 `GET` | [GetExchangeRateByCurrencyId](#getexchangeratebycurrencyid) | Returns the daily exchange rate for the specified currency. |

## Kazalo metod

- 🟢 [GetExchangeRateByCurrencyCode](#getexchangeratebycurrencycode)
- 🟢 [GetExchangeRateByCurrencyId](#getexchangeratebycurrencyid)

---

## Podrobnosti metod

### GetExchangeRateByCurrencyCode

🟢 **GET** &nbsp;`api/orgs/{organisationId}/exchange-rates/code({currencyCode})?date={date}`

Returns the daily exchange rate for the currency that corresponds with the specified code.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-exchange-rates-code(currencyCode)_date)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `currencyCode` | The currency code. |
| `date` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Date` | Exchange rate date. |
| `Currency` | class Currency. Currency. |
| `MidRate` | Middle exchange rate. |

---

### GetExchangeRateByCurrencyId

🟢 **GET** &nbsp;`api/orgs/{organisationId}/exchange-rates/{currencyId}?date={date}`

Returns the daily exchange rate for the specified currency.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-exchange-rates-currencyId_date)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |
| `currencyId` | The currency id. |
| `date` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Date` | Exchange rate date. |
| `Currency` | class Currency. Currency. |
| `MidRate` | Middle exchange rate. |

---
