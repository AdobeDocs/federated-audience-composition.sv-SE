---
title: Kom igång med Federated Audience Composition
description: Lär dig vad Adobe Federated Audience Composition är och hur du använder det i Adobe Experience Platform
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 6cfd3bd85d7811e00e716042502c7d7b23fa4ad9
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 1%

---


# Kom igång med Federated Audience Composition {#gs-fac}

Federated Audience Composition Composition är ett tillägg för Adobe Real-time Customer Data Platform och Adobe Journey Optimizer som gör det möjligt att skapa och berika målgrupper från externa datalager och importera målgrupperna till Adobe Experience Platform. Med Federated Audience Composition får du en enkel och kraftfull lösning för att ansluta företagets datalager direkt inom Adobe Real-time Customer Data Platform och/eller Adobe Journey Optimizer och utföra frågor i datalagrets tabeller.

Adobe Federated Audience Composition hjälper Adobe Experience Platform-appanvändare att få tillgång till sina kunddata som lagras i datalagret och molnlagringsplattformar som Amazon Redshift, Azure synapse Analytics med flera. Kunddata kan lagras i flera datalager och är nu tillgängliga direkt, utan replikering. Plattformar som stöds listas på [den här sidan](../connections/federated-db.md#supported-db).

## Användningsfall {#rn-uc}

Med ett marknadsföringsvänligt användargränssnitt kan du skapa segmentregler som söker efter en lista på de användare som är kvalificerade för ett visst segment som behövs för marknadsföringskampanjer, få tillgång till befintliga målgrupper i lagerstället för aktivering eller berika Adobe Experience Platform-målgrupper med ytterligare datapunkter som finns i lagerstället.

I den här versionen finns två användningsexempel: Målgruppssegmentering och målgruppsberikning. Profilberikning kommer att finnas i en framtida version.

![diagram](assets/fac-use-cases.png){zoomable="yes"}

## Viktiga steg {#gs-steps}

Med Adobe Federated Audience Composition kan ni skapa och uppdatera Adobe Experience Platform-målgrupper direkt från er databas, utan att behöva lägga in något i den.

![diagram](assets/steps-diagram.png){zoomable="yes"}

Viktiga steg:

1. **Dataintegrering**: Samla data från olika källor och sammanfoga dem i en enhetlig datauppsättning. Lär dig hur du ansluter Adobe Experience Platform-program och ditt företagsdatalager, databaser som stöds och hur du konfigurerar dem finns i [det här avsnittet](../connections/federated-db.md).

2. **Datamodellering**: Designa och skapa datamodeller och scheman som definierar datastrukturen, relationerna och begränsningarna. Läs mer om scheman på [den här sidan](../customer/schemas.md). Lär dig hur du skapar länkar för din datamodell på [den här sidan](../data-management/gs-models.md).

3. **Dataomvandling**: Använd dataändringstekniker för att ändra dataelementens format, struktur eller värden så att de blir kompatibla eller lämpliga för specifika analyser eller program.

4. **Dataanvändning**: Skapa, samordna och skapa målgrupper. Lär dig hur du skapar målgrupper på [den här sidan](../compositions/gs-compositions.md). Ni kan också uppdatera eller återanvända befintliga målgrupper via Adobe Experience Platform Audience Portal och Destinations. Läs mer på [den här sidan](../connections/destinations.md)



## Läs mer {#learn}

<!-- Workflow + Workflow activities-->

Se Vanliga frågor och svar på [den här sidan](faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Körningsinställningar"
>abstract="I det här avsnittet kan du konfigurera inställningar som är relaterade till arbetsflödets körning, t.ex. antalet dagar som kompositionshistoriken sparas."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktiviteten är inte redigerbar"
>abstract="När en **fråga** eller en **berikning**-aktivitet har konfigurerats med ytterligare data i konsolen, beaktas data för berikning och skickas till den utgående övergången, men den kan inte redigeras."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Skapa en länk"
>abstract="Definiera länkinställningarna."
