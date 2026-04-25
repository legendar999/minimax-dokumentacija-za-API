# Organisation

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Organisation](https://moj.minimax.si/SI/API/Home/ModuleDetails/Organisation)  
> **Generirano:** 25. 04. 2026 ob 12:15  
> [← Nazaj na kazalo](../README.md)

---

## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetAllOrganisations](#getallorganisations) | Returns all organizations details. |
| 2 | 🟢 `GET` | [GetOrganisation](#getorganisation) | Returns organisation details. |

## Kazalo metod

- 🟢 [GetAllOrganisations](#getallorganisations)
- 🟢 [GetOrganisation](#getorganisation)

---

## Podrobnosti metod

### GetAllOrganisations

🟢 **GET** &nbsp;`api/orgs/allOrgs?startRowIndex={startRowIndex}&endRowIndex={endRowIndex}&searchString={searchString}`

Returns all organizations details.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-allOrgs_startRowIndex_endRowIndex_searchString)

#### Request parametri

| Property | Description |
| --- | --- |
| `startRowIndex` |  |
| `endRowIndex` |  |
| `searchString` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Capacity` |  |
| `Count` |  |
| `Item` | class Organisation. |

---

### GetOrganisation

🟢 **GET** &nbsp;`api/orgs/{organisationId}`

Returns organisation details.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` |  |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `OrganisationId` | Organisation id. |
| `Title` | Organisation title. |
| `Address` | Organisation address. |
| `PostalCode` | Organisation postal code. |
| `City` | Organisation city. |
| `Country` | class Country. Organisation country. |
| `TaxNumber` | Organisation tax number. |
| `RegistrationNumber` | Organisation registration number. |
| `VATIdentificationNumber` | Organisation VAT identification number. |
| `Administrator` | class User. User according to the status of administrator. |
| `Status` | Possible values: (X, B, V). Status:   V – Activated B - Deleted |
| `RecordDtModified` |  |
| `RowVersion` | Row version is used for concurrency check. |

---
