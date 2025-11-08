---
title: Nyheter i Experience Platform Federated Audience Composition
description: Senaste uppdateringar och versionsinformation
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: aabe96fc223af5841c7b77ab914745d08d82ce49
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 3%

---

# Versionsinformation {#rn-new}

[!DNL Federated Audience Composition] levererar kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar. Alla ändringar konsolideras i versionsinformationen. [!DNL Federated Audience Composition] är inbyggd i [!DNL Adobe Experience Platform] och ärver från de senaste innovationerna och förbättringarna. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=sv-SE){target="_blank"}.

## 25 oktober {#fac-25-10}

### Nya funktioner {#fac-25-10-feature}

<!-- 
<table>
<thead>
<tr>
<th><strong>Availability for Adobe Experience Platform customers on Amazon Web Services (AWS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use Federated Audience Composition if your Experience Platform instance is on AWS.</p>
<p>For more information about Experience Platform on AWS, please read the <a href="https://experienceleague.adobe.com/sv/docs/experience-platform/landing/multi-cloud">multi-cloud overview</a>.</p>
</br>
</td>
</tr>
</tbody>
</table> 
-->

<table>
<thead>
<tr>
<th><strong>OAuth-autentisering för Google BigQuery och Snowflake</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du ansluta till Google BigQuery och Snowflake med OAuth.</p>
<p>Mer information om hur du skapar anslutningar finns i <a href="../connections/home.md#create">anslutningsöversikten</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

## Version 25 augusti {#fac-25-8}

### Nya funktioner {#fac-25-08-feature}

<table>
<thead>
<tr>
<th><strong>Stöd för sammansatta nycklar vid schemaidentifiering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du kombinera kolumner för att skapa en sammansatt nyckel för ditt schema.</p>
<p>Mer information om scheman finns i översikten <a href="../customer/schemas.md#create">scheman</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lägga till flera kopplingar i en länk för modeller</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du lägga till flera sammanfogningar i en enda länk för dina modeller.</p>
<p>Mer information om modeller finns i <a href="../data-management/gs-models.md#create">modellöversikten</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Förbättringar {#fac-25-8-improvements}

Den här versionen innehåller följande förbättringar:

* **Tillagd `StringAgg`-funktion**

  Du kan nu använda funktionen `StringAgg` för Amazon Redshift Spectrum-databaser när. med uttrycksredigeraren.

* **`Replace`funktion**

  Funktionens beskrivning och syntax för `Replace` har förtydligats i dokumentationen.

### Kompatibilitet {#fac-25-8-compatibility}

* **Azure Synapse-databaser**

  Nu kan du ansluta säkert till Azure Synapse-databaser med PrivateLink eller VPN. Kontakta Adobe kundtjänst om du vill ha mer information.

* **Oracle-databas**

  Nu kan du ansluta säkert till Oracle-databaser. Kontakta Adobe kundtjänst om du vill ha mer information.

Mer information om vilka databaser som stöds i Federated Audience Composition finns i [anslutningsöversikten](../connections/home.md).

## Version 25 juli {#fac-25-7}

### Nya funktioner {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>Ny anslutning - Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oracle-anslutningen är nu tillgänglig för användning med Federated Audience Composition.</p>
<p>Du kan använda Oracle Connector för att skapa och berika målgrupper.</p>
<p>Mer information om Oracle-anslutningen finns i <a href="../connections/home.md#create">anslutningsöversikten</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dispositionsvarningar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Du kan nu prenumerera på aviseringar för att få veta mer om att din komposition har lyckats och misslyckats</p>
<p>Mer information om att prenumerera på meddelanden för dispositionskörningar finns i <a href="../compositions/start-monitor-composition.md#alerts">Starta och övervaka dispositionsguiden</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Förbättringar {#fac-25-07-improvements}

Den här versionen innehåller följande förbättring:

* **Utökad teckenlängd för server**

  När du konfigurerar dina externa databaser kan du nu använda upp till 255 tecken i stället för de 80 föregående tecknen.

## 25 juni {#fac-25-6}

### Förbättringar {#fac-25-06-improvements}

Den här versionen innehåller följande förbättringar:

* **Allmän tillgänglighet för kunder som använder Adobe Healthcare Shield**

  Federated Audience Composition kommer att vara tillgängligt för kunder som använder Adobe Healthcare Shield för att skapa, berika och berika målgrupper före slutet av juni.

  Mer information om sekretess och säkerhet i Federated Audience Composition finns i [Datastyrning, sekretess och säkerhetsguiden](/help/governance-privacy-security/home.md).

* **Åtkomstkontroll på objektnivå**

  Federated Audience Composition har nu stöd för åtkomstkontroll på objektnivå för att använda åtkomstetiketter på dina angivna kompositioner.

  Mer information om hur du använder åtkomstetiketter på objektnivå finns i [kompositionsguiden](/help/compositions/gs-compositions.md).

* **Standardroller**

  Du kan nu använda en av standardrollerna för att hantera användarbehörigheter för sammanställningsåtkomst för federerad publik.

  Mer information om standardrollerna finns i guiden [kom åt federerad målgruppskomposition](/help/governance-privacy-security/access-control.md).

* **Inkrementella uppdateringar i användningsfall för profilberikning**

  Aktiviteten Spara profiler har nu stöd för inkrementella uppdateringar. Med inkrementella uppdateringar kan du söka efter och uppdatera inkrementella data samtidigt som du förbättrar profiler med data från externa datalager.

  Mer information om hur du använder aktiviteten Spara profiler finns i [aktivitetsguiden för att spara profiler](/help/compositions/activities/save-profiles.md).

## Version 25 maj {#fac-25-5}

### Nya funktioner {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>Datamodellens arbetsytevy - allmän tillgänglighet</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Datamodellen med Canvas-vyn är nu tillgänglig för alla kunder!</p>
<p>Arbetsytans vy för avsnittet Datamodeller förbättrar upplevelsen genom att aktivera visualisering av datamodeller och deras länkar i en arbetsytelayout, tillsammans med den befintliga tabellvyn. </p>
<p>Mer information om arbetsytans vy finns i översikten över <a href="../data-management/gs-models.md">datamodeller</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Förbättringar {#fac-25-5-improvements}

Den här versionen innehåller följande förbättringar.

* **Rollbaserad åtkomstkontroll**

  Från och med majversionen stöder [!DNL Federated Audience Composition] nya detaljerade behörigheter för åtkomstkontroll. Användare kan tilldela dessa behörigheter till användarroller för mer exakt åtkomst till [!DNL Federated Audience Composition].

  Läs [Åtkomsthandboken för federerad målgruppskomposition](/help/governance-privacy-security/access-control.md) om du vill veta mer om de nya behörigheterna.

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
  [Läs mer om etiketter för dataanvändning](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/labels/user-guide)

### Kompatibilitet {#fac-25-4-compat}

* **Säker anslutning för Amazon Redshift**

  Med den här nya versionen har Federated Audience Composition stöd för säkra privata länkanslutningar till Amazon Redshift-databaser. [Läs mer](../connections/home.md#amazon-redshift)

* **Google BigQuery**

  I den här nya versionen har Federated Audience Composition stöd för säkra VPN-anslutningar till Google BigQuery-databaser. [Läs mer](../connections/home.md#google-bigquery)

## 25 mars-utgåvan {#fac-25-3}

### Förbättringar {#fac-25-3-improvements}

Den här versionen innehåller förbättringarna nedan.

* **Sammansättningsbehörigheter för sammansatta målgrupper**

  Från och med mars-versionen kommer [!DNL Federated Audience Composition] att börja genomdriva åtkomsten av gränssnitten **Federated datahantering** och **Federated kompositioner** för användare som har beviljats behörigheten **Hantera Federated data**.

  Vi rekommenderar att användare kontaktar administratörerna för att få denna behörighet tillagd i rollen för att kunna fortsätta använda användargränssnittet för [!DNL Federated Audience Composition].

  Mer information om hur du tilldelar den här behörigheten finns i [den detaljerade dokumentationen](/help/governance-privacy-security/access-control.md).

### Kompatibilitet {#fac-25-3-compat}

* **Databriksanslutning**

  I den här nya versionen har Federated Audience Composition nu stöd för privata länkanslutningar för databasanslutningar för databaser.
Detta inkluderar säkra anslutningar till databaser som lagras på Amazon Web Services (AWS) via privata länkar och databaser som lagras på Microsoft Azure via VPN. [Läs mer](../connections/home.md#databricks)

* **Stöd för CDP-kunder inom B2B**

  Federated Audience Composition är nu tillgängligt för B2B-kunder (Business-to-Business) som använder CDP (Customer Data Platform) för personbaserade målgruppssituationer.

* **Snowflake säker anslutning**

  Med den här nya versionen har Federated Audience Composition stöd för säkra privata länkanslutningar till Snowflake-databaser på Microsoft Azure. [Läs mer](../connections/home.md#snowflake)

## 25 februari {#fac-25-2}

Den här versionen innehåller de ändringar som anges nedan.

* **Stöd för Microsoft Fabric**

  Nu kan du upprätta anslutningar till Microsoft Fabric-databaser via Federated Audience Composition. [Läs mer](../connections/home.md)

* **Stöd för Amazon Redshift Spectrum**

  Amazon Redshift Spectrum stöds nu för Amazon Redshift-databasanslutningar. [Läs mer](../connections/home.md#amazon-redshift)

* **Förbättrad funktion för att skapa schema**

  Processen med att skapa scheman har förbättrats med ett uppdaterat användargränssnitt som är mer intuitivt och enklare att navigera i. Dessa förbättringar ger datapersonal ett smidigare och effektivare sätt att utveckla datamodeller. [Läs mer](../customer/schemas.md)

* **Stöd för målgruppsanpassning för databaser**

  Nu kan du använda Databricks i Läs målgrupp, vilket aktiverar aktiviteten för databaser och gör att den kan ställas in som en ny destination. [Läs mer](../connections/destinations.md)

## 24 november {#fac-24-11}

### Förbättringar {#fac-24-11-improvements}

Den här versionen innehåller förbättringen nedan.

* **IP-adressen tillåtelselista**

  När du lägger till en federerad databas i Adobe Experience Platform användargränssnitt kan du nu direkt visa de IP-adresser som är kopplade till dina Federated Audience Composition-instanser. På så sätt kan du enkelt kopiera och godkänna dessa IP-adresser för att ansluta till databasen, vilket ger bättre säkerhet och flexibilitet. [Läs mer](../connections/home.md)

## 24 oktober {#fac-24-10}

>[!AVAILABILITY]
>
>Adobe Experience Platform Federated Audience Composition Composition är tidigare tillgängligt för en uppsättning organisationer (LA) och är nu tillgängligt för alla användare (GA). Den här funktionen aktiveras baserat på ditt erbjudande och visas endast med tillhörande behörigheter. [Läs mer](access-prerequisites.md)

### Kompatibilitet {#fac-24-10-compat}

Med den här nya versionen är Federated Audience Composition nu kompatibelt med de system som listas nedan.

* **Stöd för databaser**

  Nu kan du upprätta anslutningar till databaser via Federated Audience Composition. [Läs mer](../connections/home.md#databricks)

* **Stöd för säker åtkomst till Snowflake via AWS PrivateLink**

  Nu stöds säker åtkomst till ditt externa Snowflake-datalager via privat länk. Observera att ditt Snowflake-konto måste finnas på Amazon Web Services (AWS) och i samma region som din Federated Audience Composition-miljö. Kontakta din Adobe-representant för att få hjälp med att konfigurera säker åtkomst till ditt Snowflake-konto. [Läs mer](../connections/home.md#snowflake)

* **Stöd för Amazon Redshift Serverless**

  Med den här nya versionen har Federated Audience Composition stöd för [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Förbättringar {#fac-24-10-improvements}

Den här versionen innehåller de förbättringar som anges nedan.

* **Uppdatera befintliga scheman**

  När en kolumn skapas, ändras eller tas bort i en federerad databas kan du nu identifiera och tillämpa ändringarna genom att klicka på knappen **[!UICONTROL Refresh schema]** i motsvarande schema. [Läs mer](../customer/schemas.md#schema-refresh)

* **Koppla en datamodell till en ny komposition**

  När du skapar en komposition kan du nu välja den datamodell som ska kopplas till den. Med det här nya alternativet är det enklare att konfigurera dina aktiviteter eftersom endast tabeller i den associerade datamodellen är tillgängliga. [Läs mer](../compositions/create-composition.md)

## Version 24 juli - Federated Audience Composition (LA) {#fac-la}

Federated Audience Composition ger företag flexibel och utökad åtkomst till datalager i företagsklass för att sätta samman målgrupper med kritiska företagsdatauppsättningar och starka varumärkesinitierade och aktuella upplevelser. Med den här nya metoden, som [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/sv/docs/experience-platform/segmentation/home){target="_blank"}- och/eller [Adobe Journey Optimizer](https://experienceleague.adobe.com/sv/docs/journey-optimizer/using/ajo-home){target="_blank"} -användare, kan du federera målgruppsdata direkt från ditt befintliga datalager för att berika Adobe Experience Platform målgrupper i ett system.

Federated Audience Composition tillgodoser de växande marknadskraven för företag som behöver flexibiliteten att kunna sätta samman målgrupper med lageruppsättningar. På så sätt kan företag minska dataflytten och samtidigt göra viktiga målgruppsdata tillgängliga för marknadsföringsteam så att de kan uppfylla kraven på användningsfall och hantera personaliserade upplevelser.

Läs mer om funktionerna för federerad målgruppskomposition på [den här sidan](get-started.md) och i [Vanliga frågor](faq.md).

Detaljerad information om förutsättningarna för att komma åt Federated Audience Compositions och aktuella skyddsutkast finns på [den här sidan](access-prerequisites.md).
