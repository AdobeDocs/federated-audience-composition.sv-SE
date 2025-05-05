---
title: Nyheter i Experience Platform Federated Audience Composition
description: Senaste uppdateringar och versionsinformation
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 5%

---

# Versionsinformation {#rn-new}

[!DNL Federated Audience Composition] levererar kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar. Alla ändringar konsolideras i versionsinformationen. [!DNL Federated Audience Composition] är inbyggd i [!DNL Adobe Experience Platform] och ärver från de senaste innovationerna och förbättringarna. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## 25 april {#fac-25-4}

### Nya funktioner {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>Datamodellens arbetsytevy - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Arbetsytans vy för avsnittet Datamodeller förbättrar upplevelsen genom att aktivera visualisering av datamodeller och deras länkar i en arbetsytelayout, tillsammans med den befintliga tabellvyn. </p>
<p>Datamodellen med Canvas-vyn är för närvarande tillgänglig som en betaversion för att endast välja användare.</p>
<p>Mer information finns i den <a href="../data-management/gs-models.md">detaljerade dokumentationen</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant-stöd för produktkunskap</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI Assistant är en gränssnittsfunktion som hjälper dig att navigera i och förstå Adobe koncept och få driftsinsikter för just din miljö. Det finns i flera Adobe Experience Cloud-produkter, inklusive Federated Audience Composition.</p>
<p>Mer information finns i den <a href="../start/ai-assistant.md">detaljerade dokumentationen</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Spara profilaktivitet</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> Federated Audience Composition har nu stöd för profilberikning, vilket gör att man kan förbättra befintliga Experience Platform-profiler med data från externa datalager.
</p>
<p>Mer information finns i den <a href="../compositions/activities/save-profiles.md">detaljerade dokumentationen</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Förbättringar {#fac-25-4-improvements}

Den här versionen innehåller förbättringarna nedan.

* **Datamodellnamn**

  På menyn Publiker visar nu fliken **Federerade kompositioner** datamodellens namn i stället för ID, vilket förbättrar tydligheten och den övergripande användbarheten.

* **Målgrupp**

  På menyn Målgrupp visas nu namnet eller etiketten för den valda datamodellen när en användare väljer en datamodell utan tillhörande målgrupper.

* **Export till stora målgrupper**

  Federated Audience Composition har nu stöd för export av stora målgrupper med filstorlekar större än 1 GB.

* **Spara målgruppsaktivitet**

  En anteckning har lagts till i aktiviteten **Spara målgrupp**, som påminner användarna om att samarbeta med en dataadministratör för att använda styrningsetiketter på nya scheman och datauppsättningar som skapas när målgrupper skapas och berikas.
  [Läs mer om etiketter för dataanvändning](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/user-guide)

### Kompatibilitet {#fac-25-4-compat}

* **Säker anslutning för Amazon Redshift**

  Med den här nya versionen har Federated Audience Composition stöd för säkra privata länkanslutningar till Amazon Redshift-databaser. [Läs mer](../connections/federated-db.md#amazon-redshift)

* **Google Big Query**

  I den här nya versionen har Federated Audience Composition stöd för säkra VPN-anslutningar till Google Big Query-databaser. [Läs mer](../connections/federated-db.md#google-big-query)

## 25 mars-utgåvan {#fac-25-3}

### Förbättringar {#fac-25-3-improvements}

Den här versionen innehåller förbättringarna nedan.

* **Sammansättningsbehörigheter för sammansatta målgrupper**

  Från och med mars-versionen kommer [!DNL Federated Audience Composition] att börja genomdriva åtkomsten av gränssnitten **Federated datahantering** och **Federated kompositioner** för användare som har beviljats behörigheten **Hantera Federated data**.

  Vi rekommenderar att användare kontaktar administratörerna för att få denna behörighet tillagd i rollen för att kunna fortsätta använda användargränssnittet för [!DNL Federated Audience Composition].

  Mer information om hur du tilldelar den här behörigheten finns i [den detaljerade dokumentationen](feature-access.md).

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. 
-->


### Kompatibilitet {#fac-25-3-compat}

* **Databriksanslutning**

  I den här nya versionen har Federated Audience Composition nu stöd för privata länkanslutningar för databasanslutningar för databaser.
Detta inkluderar säkra anslutningar till databaser som lagras på Amazon Web Services (AWS) via privata länkar och databaser som lagras på Microsoft Azure via VPN. [Läs mer](../connections/federated-db.md#databricks)

* **Stöd för CDP-kunder inom B2B**

  Federated Audience Composition är nu tillgängligt för B2B-kunder (Business-to-Business) som använder CDP (Customer Data Platform) för personbaserade målgruppssituationer.

* **Snowflake säker anslutning**

  Med den här nya versionen har Federated Audience Composition stöd för säkra privata länkanslutningar till Snowflake-databaser på Microsoft Azure. [Läs mer](../connections/federated-db.md#snowflake)

## 25 februari {#fac-25-2}

Den här versionen innehåller de ändringar som anges nedan.

* **Stöd för Microsoft Fabric**

  Nu kan du upprätta anslutningar till Microsoft Fabric-databaser via Federated Audience Composition. [Läs mer](../connections/federated-db.md)

* **Stöd för Amazon Redshift Spectrum**

  Amazon Redshift Spectrum stöds nu för Amazon Redshift-databasanslutningar. [Läs mer](../connections/federated-db.md#amazon-redshift)

* **Förbättrad funktion för att skapa schema**

  Processen med att skapa scheman har förbättrats med ett uppdaterat användargränssnitt som är mer intuitivt och enklare att navigera i. Dessa förbättringar ger datapersonal ett smidigare och effektivare sätt att utveckla datamodeller. [Läs mer](../customer/schemas.md)

* **Stöd för målgruppsanpassning för databaser**

  Nu kan du använda Databricks i Läs målgrupp, vilket aktiverar aktiviteten för databaser och gör att den kan ställas in som en ny destination. [Läs mer](../connections/destinations.md)

## 24 november {#fac-24-11}

### Förbättringar {#fac-24-11-improvements}

Den här versionen innehåller förbättringen nedan.

* **IP-adressen tillåtelselista**

  När du lägger till en federerad databas i Adobe Experience Platform användargränssnitt kan du nu direkt visa de IP-adresser som är kopplade till dina Federated Audience Composition-instanser. På så sätt kan du enkelt kopiera och godkänna dessa IP-adresser för att ansluta till databasen, vilket ger bättre säkerhet och flexibilitet. [Läs mer](../connections/connections.md)

## 24 oktober {#fac-24-10}

>[!AVAILABILITY]
>
>Adobe Experience Platform Federated Audience Composition Composition är tidigare tillgängligt för en uppsättning organisationer (LA) och är nu tillgängligt för alla användare (GA). Den här funktionen aktiveras baserat på ditt erbjudande och visas endast med tillhörande behörigheter. [Läs mer](access-prerequisites.md)
>

### Kompatibilitet {#fac-24-10-compat}

Med den här nya versionen är Federated Audience Composition nu kompatibelt med de system som listas nedan.

* **Stöd för databaser**

  Nu kan du upprätta anslutningar till databaser via Federated Audience Composition. [Läs mer](../connections/federated-db.md#databricks)

* **Stöd för säker åtkomst till Snowflake via AWS PrivateLink**

  Nu stöds säker åtkomst till ditt externa Snowflake-datalager via privat länk. Observera att ditt Snowflake-konto måste finnas på Amazon Web Services (AWS) och i samma region som din Federated Audience Composition-miljö. Kontakta din Adobe-representant för att få hjälp med att konfigurera säker åtkomst till ditt Snowflake-konto. [Läs mer](../connections/federated-db.md#snowflake)

* **Stöd för Amazon Redshift Serverless**

  Med den här nya versionen har Federated Audience Composition stöd för [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Förbättringar {#fac-24-10-improvements}

Den här versionen innehåller de förbättringar som anges nedan.

* **Uppdatera befintliga scheman**

  När en kolumn skapas, ändras eller tas bort i en federerad databas kan du nu identifiera och tillämpa ändringarna genom att klicka på knappen **[!UICONTROL Refresh schema]** i motsvarande schema. [Läs mer](../customer/schemas.md#schema-refresh)

* **Koppla en datamodell till en ny komposition**

  När du skapar en komposition kan du nu välja den datamodell som ska kopplas till den. Med det här nya alternativet är det enklare att konfigurera dina aktiviteter eftersom endast tabeller i den associerade datamodellen är tillgängliga. [Läs mer](../compositions/create-composition.md)

## Version 24 juli - Federated Audience Composition (LA) {#fac-la}

Federated Audience Composition ger företag flexibel och utökad åtkomst till datalager i företagsklass för att sätta samman målgrupper med kritiska företagsdatauppsättningar och starka varumärkesinitierade och aktuella upplevelser. Med den här nya metoden, som [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"}- och/eller [Adobe Journey Optimizer](https://experienceleague.adobe.com/sv/docs/journey-optimizer/using/ajo-home){target="_blank"} -användare, kan du federera målgruppsdata direkt från ditt befintliga datalager för att berika Adobe Experience Platform målgrupper i ett system.

Federated Audience Composition tillgodoser de växande marknadskraven för företag som behöver flexibiliteten att kunna sätta samman målgrupper med lageruppsättningar. På så sätt kan företag minska dataflytten och samtidigt göra viktiga målgruppsdata tillgängliga för marknadsföringsteam så att de kan uppfylla kraven på användningsfall och hantera personaliserade upplevelser.

Läs mer om funktionerna för federerad målgruppskomposition på [den här sidan](get-started.md) och i [Vanliga frågor](faq.md).

Detaljerad information om förutsättningarna för att komma åt Federated Audience Compositions och aktuella skyddsutkast finns på [den här sidan](access-prerequisites.md).
