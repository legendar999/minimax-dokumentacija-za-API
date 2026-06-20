# Minimax API — Dokumentacija

> **Vir:** [https://moj.minimax.si/SI/API](https://moj.minimax.si/SI/API)  
> **Generirano:** 25. 04. 2026 ob 12:16

---

## ⚠️ Pravno obvestilo / Disclaimer

To je **neuradna** kopija oz. predelava javno dostopne API dokumentacije računovodskega sistema **Minimax**, urejena za lažje podajanje v AI modele. **Ni** uraden repozitorij in **ni** povezan ali potrjen s strani Minimaxa.

Vse avtorske pravice do izvorne vsebine pripadajo podjetju **Minimax / Seyfor d.o.o.** Vsebina je tu zgolj za priročnost; merodajen je vedno uradni vir: [moj.minimax.si/SI/API](https://moj.minimax.si/SI/API).

Ker avtorske pravice do te vsebine niso moje, repozitorij **ni** opremljen z licenco za odprto kodo — gradiva ne morem licencirati. Za pogoje uporabe glejte uradne pogoje Minimaxa.

---

## Splošne informacije

- Home
- ChangeLog
- Terms of use
- Swagger UI
- Account
- Address
- Analytic
- BankAccount
- Contact
- Country
- Currency
- Customer
- Dashboard
- Document
- DocumentNumbering
- Employee
- ExchangeRate
- Inbox
- IssuedInvoice
- IssuedInvoicePosting
- Item
- Journal
- JournalType
- Order
- Organisation
- Outbox
- PaymentMethod
- PayrollSettings
- PostalCode
- ProductGroup
- PurposeCode
- ReceivedInvoice
- ReportTemplate
- Stock
- StockEntry
- User
- VatAccountingType
- VatRate
- Warehouse

### Minimax API

You can get more information about Minimax API on Minimax help page.

#### API System Limits

##### Requests

- There is a daily limit of 1,000 API calls that a provider can make against a particular organisation in a rolling 24 hour period for each organisation connected to.
- There is a monthly limit of 20,000 API calls that a provider can make against a particular organisation in month period for each organisation connected to.

##### Created objects

- Minimax API is designed for volumes up to 1,000 issued invoices and proforma invoices per month.
- Minimax API is designed for volumes up to 1,000 stock entries per month.
- Minimax API is designed for volumes up to 50,000 jounal entry rows per month.
- Minimax API is designed for volumes up to 1,000 orders per month.


## OAuth2 Avtorizacija

| Endpoint | URL |
| --- | --- |
| Authorization | `https://moj.minimax.si/SI/AUT/OAuth20` |
| Token | `https://moj.minimax.si/SI/AUT/OAuth20/Token` |

---

## Kazalo modulov

| # | Modul | Metod | Opis |
| --- | --- | --- | --- |
| 1 | [Account](Account/Account.md) | 5 |  |
| 2 | [Address](Address/Address.md) | 6 |  |
| 3 | [Analytic](Analytic/Analytic.md) | 6 |  |
| 4 | [BankAccount](BankAccount/BankAccount.md) | 6 |  |
| 5 | [Contact](Contact/Contact.md) | 7 |  |
| 6 | [Country](Country/Country.md) | 4 |  |
| 7 | [Currency](Currency/Currency.md) | 5 |  |
| 8 | [Customer](Customer/Customer.md) | 8 |  |
| 9 | [Dashboard](Dashboard/Dashboard.md) | 1 |  |
| 10 | [Document](Document/Document.md) | 10 |  |
| 11 | [DocumentNumbering](DocumentNumbering/DocumentNumbering.md) | 2 |  |
| 12 | [Employee](Employee/Employee.md) | 6 |  |
| 13 | [ExchangeRate](ExchangeRate/ExchangeRate.md) | 2 |  |
| 14 | [Inbox](Inbox/Inbox.md) | 7 |  |
| 15 | [IssuedInvoice](IssuedInvoice/IssuedInvoice.md) | 10 |  |
| 16 | [IssuedInvoicePosting](IssuedInvoicePosting/IssuedInvoicePosting.md) | 6 |  |
| 17 | [Item](Item/Item.md) | 10 |  |
| 18 | [Journal](Journal/Journal.md) | 12 |  |
| 19 | [JournalType](JournalType/JournalType.md) | 4 |  |
| 20 | [Order](Order/Order.md) | 8 |  |
| 21 | [Organisation](Organisation/Organisation.md) | 2 |  |
| 22 | [Outbox](Outbox/Outbox.md) | 2 |  |
| 23 | [PaymentMethod](PaymentMethod/PaymentMethod.md) | 1 |  |
| 24 | [PayrollSettings](PayrollSettings/PayrollSettings.md) | 1 |  |
| 25 | [PostalCode](PostalCode/PostalCode.md) | 3 |  |
| 26 | [ProductGroup](ProductGroup/ProductGroup.md) | 6 |  |
| 27 | [PurposeCode](PurposeCode/PurposeCode.md) | 4 |  |
| 28 | [ReceivedInvoice](ReceivedInvoice/ReceivedInvoice.md) | 7 |  |
| 29 | [ReportTemplate](ReportTemplate/ReportTemplate.md) | 3 |  |
| 30 | [Stock](Stock/Stock.md) | 2 |  |
| 31 | [StockEntry](StockEntry/StockEntry.md) | 7 |  |
| 32 | [User](User/User.md) | 2 |  |
| 33 | [VatAccountingType](VatAccountingType/VatAccountingType.md) | 2 |  |
| 34 | [VatRate](VatRate/VatRate.md) | 4 |  |
| 35 | [Warehouse](Warehouse/Warehouse.md) | 6 |  |

---

## Hitri dostop

- [Account](Account/Account.md) &nbsp;—&nbsp; 5 metod
- [Address](Address/Address.md) &nbsp;—&nbsp; 6 metod
- [Analytic](Analytic/Analytic.md) &nbsp;—&nbsp; 6 metod
- [BankAccount](BankAccount/BankAccount.md) &nbsp;—&nbsp; 6 metod
- [Contact](Contact/Contact.md) &nbsp;—&nbsp; 7 metod
- [Country](Country/Country.md) &nbsp;—&nbsp; 4 metod
- [Currency](Currency/Currency.md) &nbsp;—&nbsp; 5 metod
- [Customer](Customer/Customer.md) &nbsp;—&nbsp; 8 metod
- [Dashboard](Dashboard/Dashboard.md) &nbsp;—&nbsp; 1 metod
- [Document](Document/Document.md) &nbsp;—&nbsp; 10 metod
- [DocumentNumbering](DocumentNumbering/DocumentNumbering.md) &nbsp;—&nbsp; 2 metod
- [Employee](Employee/Employee.md) &nbsp;—&nbsp; 6 metod
- [ExchangeRate](ExchangeRate/ExchangeRate.md) &nbsp;—&nbsp; 2 metod
- [Inbox](Inbox/Inbox.md) &nbsp;—&nbsp; 7 metod
- [IssuedInvoice](IssuedInvoice/IssuedInvoice.md) &nbsp;—&nbsp; 10 metod
- [IssuedInvoicePosting](IssuedInvoicePosting/IssuedInvoicePosting.md) &nbsp;—&nbsp; 6 metod
- [Item](Item/Item.md) &nbsp;—&nbsp; 10 metod
- [Journal](Journal/Journal.md) &nbsp;—&nbsp; 12 metod
- [JournalType](JournalType/JournalType.md) &nbsp;—&nbsp; 4 metod
- [Order](Order/Order.md) &nbsp;—&nbsp; 8 metod
- [Organisation](Organisation/Organisation.md) &nbsp;—&nbsp; 2 metod
- [Outbox](Outbox/Outbox.md) &nbsp;—&nbsp; 2 metod
- [PaymentMethod](PaymentMethod/PaymentMethod.md) &nbsp;—&nbsp; 1 metod
- [PayrollSettings](PayrollSettings/PayrollSettings.md) &nbsp;—&nbsp; 1 metod
- [PostalCode](PostalCode/PostalCode.md) &nbsp;—&nbsp; 3 metod
- [ProductGroup](ProductGroup/ProductGroup.md) &nbsp;—&nbsp; 6 metod
- [PurposeCode](PurposeCode/PurposeCode.md) &nbsp;—&nbsp; 4 metod
- [ReceivedInvoice](ReceivedInvoice/ReceivedInvoice.md) &nbsp;—&nbsp; 7 metod
- [ReportTemplate](ReportTemplate/ReportTemplate.md) &nbsp;—&nbsp; 3 metod
- [Stock](Stock/Stock.md) &nbsp;—&nbsp; 2 metod
- [StockEntry](StockEntry/StockEntry.md) &nbsp;—&nbsp; 7 metod
- [User](User/User.md) &nbsp;—&nbsp; 2 metod
- [VatAccountingType](VatAccountingType/VatAccountingType.md) &nbsp;—&nbsp; 2 metod
- [VatRate](VatRate/VatRate.md) &nbsp;—&nbsp; 4 metod
- [Warehouse](Warehouse/Warehouse.md) &nbsp;—&nbsp; 6 metod

---

*Skupaj modulov: **35** &nbsp;|&nbsp; Skupaj metod: **177***
