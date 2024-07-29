---
title: Kom igång med Experience Platform Federated Audience Composition
description: Lär dig vad Adobe Federated Audience Composition är och hur du använder det i Adobe Experience Platform
badge: label="Begränsad tillgänglighet" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 1%

---

# Kom igång med Federated Audience Composition {#gs-fac}

Federated Audience Composition är en tilläggsfunktion för [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"} och [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home){target="_blank"} som gör att du kan skapa och berika målgrupper från externa datalager och importera målgrupper till Adobe Experience Platform. Med Federated Audience Composition får du en enkel och kraftfull lösning för att ansluta företagets datalager direkt inom Adobe Real-time Customer Data Platform och/eller Adobe Journey Optimizer och utföra frågor i datalagrets tabeller.

Adobe Federated Audience Composition hjälper Adobe Experience Platform-appanvändare att få tillgång till sina kunddata som lagras i datalagret och molnlagringsplattformar som Amazon Redshift, Azure synapse Analytics med flera. Kunddata kan lagras i flera datalager och är nu tillgängliga direkt, utan replikering. Plattformar som stöds listas på [den här sidan](../connections/federated-db.md#supported-db).

## Funktioner {#rn-capabilities}

Med Federated Audience Composition kan man utnyttja Real-Time CDP och Journey Optimizer på ett omfattande sätt:

* Utöka åtkomsten till kritiska lagerbaserade datauppsättningar för att skapa värdefulla målgrupper: Utnyttja befintliga datalager som det viktigaste systemet för register, samtidigt som ni utnyttjar förstklassiga tillämpningar för att skapa fantastiska kundupplevelser.

* Omfattande stöd för fall av strömålinriktning: Federated Audience Composition, i kombination med Real-Time CDP eller Journey Optimizer, stöder varumärkesinitierade, personaliserade upplevelser med federerade målgrupper och levererar upplevelser i realtid som triggas av händelser i realtid, kombinerat med personattribut för att uppfylla användningsbehoven i olika team.

* Minimera dataförflyttning och duplicering: Skapa målgrupper från datauppsättningar som finns i ett datalager i ett företag utan att kopiera underliggande data för att hantera användbara marknadsföringsprofiler och målgrupper.

* Använd ett enda system för upplevelsestyrda arbetsflöden: Kuratera inkapslade och federerade målgrupper i Adobe Experience Platform och koordinera utgående upplevelser i alla kanaler.

## Användningsfall {#rn-uc}

Med ett marknadsföringsvänligt användargränssnitt kan du skapa segmentregler som söker efter en lista på de användare som är kvalificerade för ett visst segment som behövs för marknadsföringskampanjer, få tillgång till befintliga målgrupper i lagerstället för aktivering eller berika Adobe Experience Platform-målgrupper med ytterligare datapunkter som finns i lagerstället.

I den här versionen finns två exempel:

1. Målgrupper: Bygg nya målgrupper från företagsdatauppsättningar utan att kopiera underliggande data och aktivera dessa målgrupper med färdiga destinationer. &#x200B;

1. Audience Enrichment: Berika befintliga målgrupper i Adobe Experience Platform genom att utnyttja sammansatta målgruppsdata som har federerats från företagets datalager. Dessa data bevaras inte i Adobe Experience Platform kundprofiler.

![diagram](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Viktiga steg {#gs-steps}

Med Adobe Federated Audience Composition kan ni skapa och uppdatera Adobe Experience Platform-målgrupper direkt från er databas, utan att behöva lägga in något i den.

![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

Viktiga steg:

1. **Dataintegrering**: Samla data från olika källor och sammanfoga dem i en enhetlig datauppsättning. Lär dig hur du ansluter Adobe Experience Platform-program och ditt företagsdatalager, databaser som stöds och hur du konfigurerar dem finns i [det här avsnittet](../connections/federated-db.md).

2. **Datamodellering**: Designa och skapa datamodeller och scheman som definierar datastrukturen, relationerna och begränsningarna. Läs mer om scheman på [den här sidan](../customer/schemas.md). Lär dig hur du skapar länkar för din datamodell på [den här sidan](../data-management/gs-models.md).

3. **Dataomvandling**: Använd dataändringstekniker för att ändra dataelementens format, struktur eller värden så att de blir kompatibla eller lämpliga för specifika analyser eller program.

4. **Dataanvändning**: Skapa, samordna och skapa målgrupper. Lär dig hur du skapar målgrupper på [den här sidan](../compositions/gs-compositions.md). Ni kan också uppdatera eller återanvända befintliga målgrupper via Adobe Experience Platform Audience Portal och Destinations. Läs mer på [den här sidan](../connections/destinations.md)

>[!NOTE]
>
>När kompositionen är klar sparas målgruppen i Adobe Experience Platform som en extern målgrupp och finns tillgänglig i Adobe Real-Time Customer Data Platform och/eller Adobe Journey Optimizer. Den är tillgänglig på menyn **Publiker** . [Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Läs mer {#learn}

<!-- Workflow + Workflow activities-->


Lär dig hur du får åtkomst till federerad målgruppskomposition, skyddsutkast och begränsningar på [den här sidan](access-prerequisites.md).

Se även vanliga frågor och svar på [den här sidan](faq.md).


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
