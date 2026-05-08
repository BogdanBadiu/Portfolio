# Selling System — Java Point-of-Sale Application

A Java desktop **Point-of-Sale (POS)** application with role-based access (Manager / Cashier), product scanning, and integrated card payment validation. Built in NetBeans with Java Swing and Apache Derby (embedded database).

## Features

- **Role-based login** — Manager and Cashier accounts with different permissions
- **Product scanning** — scan products by code (`00001` … `00005` available in seed data)
- **Card payments** — validates credit-card number and PIN against a separate `ManagerCard` database
- **Profit reporting** — manager-side profit calculation (`Profit.java`)
- **Two databases** — `Magazin` (store inventory and sales) + `ManagerCard` (cardholder data)

## Test Credentials

| Role | User | Password |
|---|---|---|
| Manager | `badiu.bogdan` | `1234` |
| Cashier | `cojocaru.gabi` | `1234` |

**Test card:** `1234-5678-1234-5678` — PIN `1234`

> Sales under 100 lei (Manager): card number only.
> Sales over 100 lei (Cashier): card number + PIN required.

## Architecture

DAO pattern with separate interface + implementation classes:

- `ProdusDao` / `Produs` — products
- `StocDaoImpl` — stock management
- `UsersDaoImpl` / `Users` — user accounts
- `DetinatorCardDaoImpl` / `DetinatorCard` — cardholders
- `InfoCardDaoImpl` / `InfoCard` — card information
- `VerificareCard` — card validation logic
- `SalesLineItem` — line items in a sale
- `TipProdus` — product type
- `ConfirmExit` — exit confirmation dialog

## Tech

Java, Swing, NetBeans (Ant build), Apache Derby (embedded JDBC database)

## Build & Run

Open the project folder in **NetBeans IDE** and run. The Ant `build.xml` is provided. Make sure both databases (`Magazin` and `ManagerCard`) are connected before attempting a sale.
