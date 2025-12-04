---
title: Behörigheter för åtkomst till en extern databas
description: Lär dig vilka behörigheter du behöver för att få åtkomst till och utföra uppgifter i varje databasmotor
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 4%

---

# Rättighetsmatris för FDA (Federated Data Access) {#fda-rights}

I följande tabell visas de databasbehörigheter som krävs för varje system, vilket gör att du kan utföra åtgärder på externa databaser via federerad dataåtkomst (FDA).

|   | Snowflake | Skift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Ansluter till fjärrdatabas** | `USAGE ON WAREHOUSE`-, `USAGE ON DATABASE`- och `USAGE ON SCHEMA`-behörigheter | Skapa en användare som är länkad till AWS-kontot | Skapa ett tjänstkonto och ge huvudkontot åtkomst till projektet | `USE CATALOG` behörighet för katalog och `CAN_USE` behörighet för SQL Warehouse |
| **Skapar tabeller** | `CREATE TABLE ON SCHEMA`-privilegium | `CREATE` behörighet | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create` och `bigquery.tables.create` behörigheter | `USE SCHEMA` och `CREATE TABLE` behörigheter |
| **Skapar index** | N/A | `CREATE` behörighet | BigQuery stöder bara sökindex. Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create`, `bigquery.tables.getData` och `bigquery.tables.createIndex` behörigheter | N/A |
| **Skapar funktioner** | `CREATE FUNCTION ON SCHEMA`-privilegium | `USAGE ON LANGUAGE plpythonu` behörighet att kunna anropa externa Python-skript | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create` och `bigquery.routines.create` behörigheter | `CREATE FUNCTION` behörighet |
| **Skapar procedurer** | N/A | `USAGE ON LANGUAGE plpythonu` behörighet att kunna anropa externa Python-skript | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create` och `bigquery.routines.create` behörigheter |  Ej tillämpligt |
| **Tar bort objekt (tabeller, index, funktioner, procedurer)** | Äga objektet | Äga objektet eller vara superanvändare | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` och `bigquery.tables.deleteIndex` behörigheter | N/A |
| **Övervaka körningar** | `MONITOR`-privilegium för det begärda objektet | Inga behörigheter krävs för att använda kommandot `EXPLAIN` | Rollen `monitoring.viewer` | `CAN_VIEW` behörighet |
| **Skriver data** | `INSERT` och/eller `UPDATE` behörigheter (beroende på skrivåtgärden) | `INSERT` och `UPDATE` behörigheter | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create` och `bigquery.tables.updateData` | `MODIFY` behörighet |
| **Läser in data i tabeller** | `CREATE STAGE ON SCHEMA`, `SELECT` och `INSERT` i måltabellens behörigheter | `SELECT` och `INSERT` behörigheter | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create`, `bigquery.tables.getData` och `bigquery.tables.updateData` | `SELECT` och `MODIFY` behörigheter |
| **Åtkomst till klientdata** | `SELECT on (FUTURE) TABLE(S)` eller `VIEW(S)` privilegium(er) | `SELECT` behörighet | Rollen som tilldelats tjänstkontot måste innehålla: `bigquery.jobs.create` och `bigquery.tables.getData` för tabeller eller rollen `bigquery.dataViewer` | `SELECT` behörighet |
| **Åtkomst till metadata** | `SELECT on INFORMATION_SCHEMA SCHEMA`-privilegium | `SELECT` behörighet | Rollen `bigquery.metadataViewer` |  `SELECT on INFORMATION_SCHEMA SCHEMA` behörighet |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Ansluter till fjärrdatabas** | Läsbehörighet (standard) | `CONNECT` behörighet | Inget privilegium krävs |
| **Skapar tabeller** | `CREATE TABLE ON DATABASE` (lagerställe) och `ALTER ON SCHEMA` | `CREATE TABLE` behörighet | `CREATE ON SCHEMA`-privilegium |
| **Skapar index** | N/A | `ALTER` behörighet | N/A |
| **Skapar funktioner** | N/A | `CREATE FUNCTION` behörighet | `CREATE ON SCHEMA`-privilegium |
| **Skapar procedurer** | `CREATE PROCEDURE ON DATABASE` (lagerställe) och `ALTER ON SCHEMA` | `CREATE PROCEDURE` behörighet | `CREATE ON SCHEMA`-privilegium |
| **Tar bort objekt (tabeller, index, funktioner, procedurer)** | `ALTER ON SCHEMA` | `ALTER` behörighet | Äger objektet eller privilegiet `DROP` för objektet |
| **Övervaka körningar** | Workspace Contributor eller högre behörigheter (`queryinsights.exec_requests_history`) | `CONTROL` behörighet | Ingen behörighet krävs för att använda programsatsen `EXPLAIN` |
| **Skriver data** | `INSERT` och/eller `UPDATE ON OBJECT` | `INSERT` och `UPDATE` behörigheter | `INSERT`- och `UPDATE`-behörigheter |
| **Läser in data i tabeller** | `SELECT ON OBJECT` och `INSERT ON OBJECT` | `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` och `ALTER` behörigheter | `INSERT`-privilegium för register, `USAGE`-privilegium för schema |
| **Åtkomst till klientdata** | `SELECT ON OBJECT` | `SELECT` behörighet | `SELECT`-privilegium |
| **Åtkomst till metadata** | `SELECT ON INFORMATION_SCHEMA` | Ingen behörighet krävs för att beskriva tabellen | `USAGE ON SCHEMA`, `SELECT on TABLE` och även behörighet för tabeller `v_catalog.columns` och `v_catalog.view_columns` |
