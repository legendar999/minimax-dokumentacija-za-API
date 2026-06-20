# Stock

> **Vir:** [https://moj.minimax.si/SI/API/Home/ModuleDetails/Stock](https://moj.minimax.si/SI/API/Home/ModuleDetails/Stock)  
> **Generirano:** 25. 04. 2026 ob 12:16  
> [← Nazaj na kazalo](../README.md)

---

> ⚠️ **Neuradno** — to je kopija javno dostopne Minimax API dokumentacije, urejena za AI. Avtorske pravice do vsebine pripadajo **Minimax / Seyfor d.o.o.**; ta repozitorij ni uraden in ni licenciran. Merodajen je uradni vir. Glej [pravno obvestilo](../README.md).


## Pregled metod

| # | HTTP | Metoda | Opis |
| --- | --- | --- | --- |
| 1 | 🟢 `GET` | [GetStockForItem](#getstockforitem) | Returns stock for item. |
| 2 | 🟢 `GET` | [GetStocks](#getstocks) | Returns all items in stock for the given organization. |

## Kazalo metod

- 🟢 [GetStockForItem](#getstockforitem)
- 🟢 [GetStocks](#getstocks)

---

## Podrobnosti metod

### GetStockForItem

🟢 **GET** &nbsp;`api/orgs/{organisationId}/stocks/{itemId}`

Returns stock for item.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-stocks-itemId)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `itemId` | item id |
| `WarehouseId` | Warehouse ID. |
| `BatchNumber` | Batch number. |
| `Date` | Date. |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Item` | class Item. Item. |
| `ItemName` | Item name. |
| `ItemCode` | Item code. |
| `ItemEANCode` | Item EAN Code. |
| `UnitOfMeasurement` | Item unit of measurement. |
| `AveragePurchasePrice` | Item average purchase price. |
| `SellingPrice` | Item selling price. |
| `Quantity` | Item quantity. |
| `Value` | Item value. |
| `BatchNumber` | Item batch number; present, if results are reported divided by batch number. |
| `Currency` | class Currency. Currency. |

---

### GetStocks

🟢 **GET** &nbsp;`api/orgs/{organisationId}/stocks`

Returns all items in stock for the given organization.

> 📖 [Originalna dokumentacija](https://moj.minimax.si/SI/API/Help/Api/GET-api-orgs-organisationId-stocks)

#### Request parametri

| Property | Description |
| --- | --- |
| `organisationId` | organisation id |
| `ItemID` | Item ID. |
| `ItemTitle` | Item Title. |
| `ItemIdentifier` | Item Identifier. |
| `ItemEANCode` | Item EANCode. |
| `ItemType` | Item Type. |
| `WarehouseId` | Warehouse ID. |
| `BatchNumber` | Batch Number. |
| `Date` | Date. |
| `ResultsByBatchNumber` | ResultsByBatchNumber. |
| `Mode` | If parameter is set to 1 the function returns all items including the items that are not in stock but were in stock at some other time. |
| `CurrentPage` | Current page index starting with 1 for first page. |
| `PageSize` | Page size defines number of records returned per page. |
| `SortField` | Field name that is used for sorting/ordering result rows. |
| `Order` | Sort order: A - ascending; D - descending |

#### Response lastnosti

| Property | Description |
| --- | --- |
| `Rows` | Returned rows. List of StockListItem. |
| `TotalRows` | Number of rows matching search condition. |
| `CurrentPageNumber` | Current page number. Result rows are returned in pages. |
| `PageSize` | Numbers of rows returned per page. |

---
