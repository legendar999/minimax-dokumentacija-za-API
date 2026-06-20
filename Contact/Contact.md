# Contact

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Contact](https://moj.minimax.si/SI/API/Home/ModuleDetails/Contact)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddContact](#addcontact) | Adds a new contact to a specified customer. |
| 2 | 🔴 `DELETE` | [DeleteContact](#deletecontact) | Deletes a contact. |
| 3 | 🟢 `GET` | [GetContact](#getcontact) | Returns a contact. |
| 4 | 🟢 `GET` | [GetContacts](#getcontacts) | Returns contacts for all customers. |
| 5 | 🟢 `GET` | [GetContactsSyncCandidates](#getcontactssynccandidates) | Returns contacts for sync. |
| 6 | 🟢 `GET` | [GetCustomerContacts](#getcustomercontacts) | Returns all contacts for a given customer. |
| 7 | 🟡 `PUT` | [UpdateContact](#updatecontact) | Updates contact information. |

## Kazalo metod

- 🔵 [AddContact](#addcontact)
- 🔴 [DeleteContact](#deletecontact)
- 🟢 [GetContact](#getcontact)
- 🟢 [GetContacts](#getcontacts)
- 🟢 [GetContactsSyncCandidates](#getcontactssynccandidates)
- 🟢 [GetCustomerContacts](#getcustomercontacts)
- 🟡 [UpdateContact](#updatecontact)

---

## Podrobnosti metod

### AddContact

🔵 **POST** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/contacts`

Adds a new contact to a specified customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-customers-customerId-contacts)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `contact` | contact data |

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

### DeleteContact

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/contacts/{contactId}`

Deletes a contact.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-customers-customerId-contacts-contactId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `contactId` | contact id |

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

### GetContact

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/contacts/{contactId}`

Returns a contact.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-contacts-contactId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `contactId` | contact id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `ContactId` | Contact id. |
| `Customer` | class Customer. Customer. |
| `FullName` | First and last name. |
| `PhoneNumber` | Telephone number. |
| `Fax` | Fax. |
| `MobilePhone` | Mobile phone. |
| `Email` | E-mail. |
| `Notes` | Notes. |
| `Default` | Default contact:
   D – Yes, N – No. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetContacts

🟢 **GET** &nbsp;`api/orgs/{organisationId}/contacts`

Returns contacts for all customers.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-contacts)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `Email` | Email. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of Contact. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetContactsSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/contacts/synccandidates`

Returns contacts for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-contacts-synccandidates)

---

### GetCustomerContacts

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/contacts`

Returns all contacts for a given customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-contacts)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `SearchString` | Search string - queries search for specified value across various predefined fields. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of Contact. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### UpdateContact

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/contacts/{contactId}`

Updates contact information.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-customers-customerId-contacts-contactId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `contactId` | contact id |
| `contact` | New contact data. |

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
