---
title: Behörigheter för åtkomst till en extern databas
description: Läs om specifika rättigheter för varje databasmotor
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 2%

---

# FDA Rights-matris {#fda-rights}

Tabellen nedan visar de databasbehörigheter som krävs för varje system, vilket gör att användare kan utföra åtgärder på externa databaser via FDA.

|   | Snowflake | Skift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Ansluter till fjärrdatabas** | ANVÄNDNING I LAGERHUS, ANVÄNDNING I DATABAS OCH ANVÄNDNING I SCHEMABEHÖRIGHETER | Skapa en användare som är länkad till AWS-kontot | Skapa ett tjänstkonto och ge huvudkontot åtkomst till projektet | Behörigheten ANVÄND KATALOG för katalog och behörigheten CAN_USE för SQL Warehouse |
| **Skapar tabeller** | Behörighet SKAPA TABELL PÅ SCHEMA | SKAPA privilegium | Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create och bigquery.tables.create permissions | Behörighet att använda SCHEMA och behörigheten SKAPA TABELL |
| **Skapar index** | N/A | SKAPA privilegium | BigQuery stöder endast sökindex. Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create, bigquery.tables.getData och bigquery.tables.createIndex-behörigheter | N/A |
| **Skapar funktioner** | SKAPA FUNKTION PÅ SCHEMABEHÖRIGHET | ANVÄNDNING PÅ SPRÅKPLAN-plypthonu-privilegium för att kunna anropa externa python-skript | Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create och bigquery.roines.create permissions | SKAPA FUNKTIONSBEHÖRIGHET |
| **Skapar procedurer** | N/A | ANVÄNDNING PÅ SPRÅKPLAN-plypthonu-privilegium för att kunna anropa externa python-skript | Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create och bigquery.roines.create permissions |  Ej tillämpligt |
| **Tar bort objekt (tabeller, index, funktioner, procedurer)** | Äga objektet | Äga objektet eller vara superanvändare | Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create, bigquery.roines.delete, bigquery.tables.delete och bigquery.tables.deleteIndex permissions |
| **Övervaka körningar** | MONITOR-behörighet för det begärda objektet | Ingen behörighet krävs för kommandot EXPLAIN | monitor.viewer-roll | Behörighet för CAN_VIEW |
| **Skriver data** | INSERT- och/eller UPDATE-behörigheter (beroende på skrivåtgärd) | INSERT- och UPDATE-behörigheter | Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create och bigquery.tables.updateData |  ÄNDRA privilegium |
| **Läser in data i tabeller** | SKAPA SCENEN I SCHEMA, MARKERA OCH INFOGA i målregisterprivilegier | VÄLJ OCH INFOGA BEHÖRIGHETER | Roll som tilldelats tjänstkontot måste innehålla: bigquery.job.create, bigquery.tables.getData och bigquery.tables.updateData | VÄLJ OCH ÄNDRA behörigheter |
| **Åtkomst till klientdata** | VÄLJ BEHÖRIGHET FÖR (FRAMTIDA) TABELL(ER) ELLER VY(ER) | VÄLJ privilegium | Rollen som tilldelas tjänstkontot måste innehålla: bigquery.job.create och bigquery.tables.getData för tabeller eller bigquery.dataViewer-rollen |  VÄLJ privilegium |
| **Åtkomst till metadata** | VÄLJ BEHÖRIGHET FÖR INFORMATION_SCHEMA SCHEMA | VÄLJ privilegium | bigquery.metadataViewer, roll |  VÄLJ BEHÖRIGHET FÖR INFORMATION_SCHEMA SCHEMA |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Ansluter till fjärrdatabas** | Läsbehörighet (standard) | CONNECT-behörighet | Inget privilegium krävs |
| **Skapar tabeller** | SKAPA TABELL PÅ DATABAS (Lagerställe) OCH ALTER PÅ SCHEMA | SKAPA TABELLBEHÖRIGHET | Behörighet SKAPA PÅ SCHEMA |
| **Skapar index** | N/A | ALTERNATIVbehörighet | N/A |
| **Skapar funktioner** | N/A | SKAPA FUNKTIONSTILLSTÅND | Behörighet SKAPA PÅ SCHEMA |
| **Skapar procedurer** | SKAPA PROCEDUR FÖR DATABAS (Lagerställe) OCH ALTER ON SCHEMA | SKAPA PROCESSTILLSTÅND | Behörighet SKAPA PÅ SCHEMA |
| **Tar bort objekt (tabeller, index, funktioner, procedurer)** | ÄNDRA PÅ SCHEMA | ALTERNATIVbehörighet | äger objektet eller DROP-privilegium för objektet |
| **Övervaka körningar** | Workspace Contributor eller högre behörigheter (queryinsights.exec_requests_history)  | BEHÖRIGHET | Inga privilegier krävs för att använda EXPLAIN-programsatsen |
| **Skriver data** | INFOGA OCH/eller UPPDATERA PÅ OBJEKT | INFOGA- och UPPDATERINGSbehörigheter | INSERT- och UPDATE-behörigheter |
| **Läser in data i tabeller** | MARKERA PÅ OBJEKT OCH INFOGA PÅ OBJEKT | SKAPA TABELL, KÖR, MARKERA, INFOGA, UPPDATERA, ALTER-behörigheter | INSERT-privilegium för register, USAGE-privilegium för schema |
| **Åtkomst till klientdata** | MARKERA PÅ OBJEKT | VÄLJ behörighet | VÄLJ privilegium |
| **Åtkomst till metadata** | VÄLJ ON INFORMATION_SCHEMA | Ingen behörighet krävs för att beskriva tabellen | USAGE ON SCHEMA, SELECT on TABLE och även behörighet för tabellerna v_catalog.columns och v_catalog.view_columns |
