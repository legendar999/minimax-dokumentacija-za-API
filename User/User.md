# User

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/User](https://moj.minimax.si/SI/API/Home/ModuleDetails/User)  
> **Generirano:** 25. 04. 2026 ob 12:16  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetCurrentUserProfile](#getcurrentuserprofile) | Returns details for current user. |
| 2 | 🟢 `GET` | [MyOrganisations](#myorganisations) | Returns a list of all organisations for current user. There you can read OrganisationId value, which you will need for c |

## Kazalo metod

- 🟢 [GetCurrentUserProfile](#getcurrentuserprofile)
- 🟢 [MyOrganisations](#myorganisations)

---

## Podrobnosti metod

### GetCurrentUserProfile

🟢 **GET** &nbsp;`api/currentuser/profile`

Returns details for current user.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-currentuser-profile)

#### Response lastnosti

| Property | Description |
| --- | --- |
| `UserId` | User id. |
| `FullName` | User name and surname. |
| `Email` | E-mail. |
| `MobilePhone` | Mobile phone. |
| `Language` | Language:
   en – English sr – Srpski sl – Slovenščina hr - Hrvatski |

---

### MyOrganisations

🟢 **GET** &nbsp;`api/currentuser/orgs`

Returns a list of all organisations for current user. There you can read OrganisationId value, which you will need for calling other miniMAX API functions.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-currentuser-orgs)

#### Request parametri

| Property | Description |
| --- | --- |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of UserOrganisation. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
