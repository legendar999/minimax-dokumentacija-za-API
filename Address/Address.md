# Address

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Address](https://moj.minimax.si/SI/API/Home/ModuleDetails/Address)  
> **Generirano:** 25. 04. 2026 ob 12:14  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🔵 `POST` | [AddAddress](#addaddress) | Adds a new address to a specific customer. |
| 2 | 🔴 `DELETE` | [DeleteAddress](#deleteaddress) | Deletes an address. |
| 3 | 🟢 `GET` | [GetAddress](#getaddress) | Returns an address. |
| 4 | 🟢 `GET` | [GetAddresses](#getaddresses) | Returns all addresses for a given customer. |
| 5 | 🟢 `GET` | [GetAddressesSyncCandidates](#getaddressessynccandidates) | Returns addresses for sync. |
| 6 | 🟡 `PUT` | [UpdateAddress](#updateaddress) | Updates an address. |

## Kazalo metod

- 🔵 [AddAddress](#addaddress)
- 🔴 [DeleteAddress](#deleteaddress)
- 🟢 [GetAddress](#getaddress)
- 🟢 [GetAddresses](#getaddresses)
- 🟢 [GetAddressesSyncCandidates](#getaddressessynccandidates)
- 🟡 [UpdateAddress](#updateaddress)

---

## Podrobnosti metod

### AddAddress

🔵 **POST** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/addresses`

Adds a new address to a specific customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/POST-api-orgs-organisationId-customers-customerId-addresses)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `address` | address data |

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

### DeleteAddress

🔴 **DELETE** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/addresses/{addressId}`

Deletes an address.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/DELETE-api-orgs-organisationId-customers-customerId-addresses-addressId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `addressId` | account id |

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

### GetAddress

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/addresses/{addressId}`

Returns an address.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-addresses-addressId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `addressId` | address id |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `AddressId` | Address id. |
| `Customer` | class Customer. Customer |
| `Type` | Possible values: (N, P). Address type:   N=Addressee; P=Recipient |
| `Name` | Name. |
| `GLN` | GLN. |
| `Address` | Address. |
| `PostalCode` | Postal code. |
| `City` | City. |
| `Country` | class Country. Country. |
| `CountryName` | Country name. |
| `Default` | Default address for given address type:   N – no, D – yes. |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---

### GetAddresses

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/addresses`

Returns all addresses for a given customer.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-addresses)

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
| `Rows` | Returned rows. List of AddressModel. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---

### GetAddressesSyncCandidates

🟢 **GET** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/addresses/synccandidates`

Returns addresses for sync.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-customers-customerId-addresses-synccandidates)

---

### UpdateAddress

🟡 **PUT** &nbsp;`api/orgs/{organisationId}/customers/{customerId}/addresses/{addressId}`

Updates an address.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/PUT-api-orgs-organisationId-customers-customerId-addresses-addressId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `customerId` | customer id |
| `addressId` | address id |
| `address` |  |

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
