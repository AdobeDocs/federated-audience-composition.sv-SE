---
title: Kom igång med Federated Audience Composition
description: Lär dig vad Adobe Federated Audience Composition är och hur du använder det i Adobe Experience Platform
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---


# Kom igång med Federated Audience Composition {#gs-fac}

Adobe Federated Audience Composition hjälper Adobe Experience Platform-appsanvändare att få tillgång till sina kunddata som lagras i företagets datalager. Kunddata kan lagras i flera datalager och bör vara tillgängliga direkt, utan replikering.

Adobe Experience Platform Federated Audience Composition erbjuder en enkel och kraftfull lösning för att ansluta företagets datalager direkt inom Adobe Real-time Customer Data Platform och utföra frågor i datalagrets tabeller.

## Viktiga steg {#gs-steps}

Med Adobe Federated Audience Composition kan ni skapa och uppdatera Adobe Experience Platform-målgrupper direkt från er databas, utan att behöva lägga in något i den.

![diagram](assets/FAC-diagram.png)

Viktiga steg:

* **Konfiguration**

   1. Koppla samman Adobe Experience Platform och företagets datalager.
Följande databaser stöds: Snowflake, Google Big Query, Azure synapse och Redshift.
Läs mer på [den här sidan](../connections/federated-db.md)
   1. Skapa scheman för att välja vilka data som ska vara tillgängliga från användargränssnittet.
Läs mer på [den här sidan](../customer/schemas.md)
   1. Skapa länkar för din datamodell.
Läs mer på [den här sidan](../data-management/gs-models.md)

* **Disponera målgrupper**

   1. Designa och kör montage för att skapa målgrupper.
Läs mer på [den här sidan](../compositions/gs-compositions.md)
   1. Uppdatera eller återanvänd befintliga målgrupper via Adobe Experience Platform Audience Portal och Destinations.
Läs mer på [den här sidan](../connections/destinations.md)

## Läs mer {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Körningsinställningar"
>abstract="I det här avsnittet kan du konfigurera inställningar som är relaterade till arbetsflödets körning, t.ex. antalet dagar som arbetsflödeshistoriken sparas."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktiviteten är inte redigerbar"
>abstract="När en **fråga** eller en **berikning**-aktivitet har konfigurerats med ytterligare data i konsolen, beaktas data för berikning och skickas till den utgående övergången, men den kan inte redigeras."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Skapa en länk"
>abstract="Definiera länkinställningarna."
