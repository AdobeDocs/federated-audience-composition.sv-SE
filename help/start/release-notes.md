---
title: Nyheter i Experience Platform Federated Audience Composition
description: Senaste uppdateringar och versionsinformation
badge: label="Begränsad tillgänglighet" type="Informative"
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 61a70f9de0a6cf171a2ff1128b57ae6206be842c
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 2%

---

# Versionsinformation {#rn-new}

[!DNL Federated Audience Composition] levererar kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar. Alla ändringar konsolideras i versionsinformationen. [!DNL Federated Audience Composition] är inbyggd i [!DNL Adobe Experience Platform] och ärver från de senaste innovationerna och förbättringarna. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## 24 oktober {#fac-24-10}

### Kompatibilitet {#fac-24-10-compat}

Med den här nya versionen är Federated Audience Composition nu kompatibelt med de system som listas nedan.

* **Stöd för databaser**

  Nu kan du upprätta anslutningar till databaser via Federated Audience Composition. [Läs mer](../connections/federated-db.md#databricks)

* **Stöd för säker åtkomst till Snowflake via AWS PrivateLink**

  Nu stöds säker åtkomst till ditt externa datalager i Snowflake via en privat länk. Observera att ditt Snowflake-konto måste finnas på Amazon Web Services (AWS) och i samma region som din Federated Audience Composition-miljö. Kontakta din Adobe-representant för att få hjälp med att skapa säker åtkomst till ditt Snowflake-konto. [Läs mer](../connections/federated-db.md#snowflake)

* **Stöd för Amazon Redshift Serverless**

  Med den här nya versionen har Federated Audience Composition stöd för [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Förbättringar {#fac-24-10-improvements}

Den här versionen innehåller de förbättringar som anges nedan.

* **Uppdatera befintliga scheman**

  När en kolumn skapas, ändras eller tas bort i en federerad databas kan du nu identifiera och tillämpa ändringarna genom att klicka på knappen **[!UICONTROL Refresh schema]** i motsvarande schema. [Läs mer](../customer/schemas.md#schema-refresh)

* **Koppla en datamodell till en ny komposition**

  När du skapar en komposition kan du nu välja den datamodell som ska kopplas till den. Med det här nya alternativet är det enklare att konfigurera dina aktiviteter eftersom endast tabeller i den associerade datamodellen är tillgängliga. [Läs mer](../compositions/create-composition.md)

## Version 24 juli - Federated Audience Composition (LA) {#fac-la}

>[!AVAILABILITY]
>
>Adobe Experience Platform Federated Audience Composition är för närvarande bara tillgängligt för en uppsättning organisationer (begränsad tillgänglighet).
>

Federated Audience Composition är en tilläggsfunktion som ger företag flexibel och utökad åtkomst till datalager i företagsklass för att skapa målgrupper med hjälp av viktiga företagsdatauppsättningar och starka varumärkesinitierade och aktuella upplevelser. Med den här nya metoden, som [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"}- och/eller [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home){target="_blank"} -användare, kan du federera målgruppsdata direkt från ditt befintliga datalager för att berika Adobe Experience Platform målgrupper i ett system.

Federated Audience Composition tillgodoser de växande marknadskraven för företag som behöver flexibiliteten att kunna sätta samman målgrupper med lageruppsättningar. På så sätt kan företag minska dataflytten och samtidigt göra viktiga målgruppsdata tillgängliga för marknadsföringsteam så att de kan uppfylla kraven på användningsfall och hantera personaliserade upplevelser. 

Läs mer om funktionerna för federerad målgruppskomposition på [den här sidan](get-started.md) och i [Vanliga frågor](faq.md).

Detaljerad information om förutsättningarna för att komma åt Federated Audience Compositions och aktuella skyddsutkast finns på [den här sidan](access-prerequisites.md).

