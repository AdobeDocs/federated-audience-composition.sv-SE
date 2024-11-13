---
audience: end-user
title: Använd anrikningsaktiviteten
description: Lär dig använda anrikningsaktiviteten
exl-id: 6bf12c25-fbef-4588-89d0-28215cbcbf58
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Berikning {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Anrikningsaktivitet"
>abstract="Med aktiviteten **Enrichment** kan du förbättra måldata med ytterligare information från databasen. Den används ofta i en komposition efter segmenteringsaktiviteter."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Anrikningsaktivitet"
>abstract="När data för berikning har lagts till i kompositionen kan de användas i aktiviteter som lagts till efter aktiviteten **Enrichment** för att segmentera profiler i distinkta grupper baserat på deras beteenden, inställningar och val."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Länkdefinition"
>abstract="Skapa en länk mellan data i arbetstabellen och den federerade databasen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Anrikningsavstämning"
>abstract="Ange avstämningsparametrarna."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Anrikningsdata"
>abstract="Välj de data som ska användas för att berika kompositionen. Du kan välja två typer av anrikningsdata: ett enskilt anrikningsattribut från schemat, även kallat måldimension, eller en samlingslänk, som är en länk med en 1-N-kardinalitet mellan tabeller."

Med aktiviteten **Enrichment** kan du förbättra måldata med ytterligare information från den federerade databasen. Den används ofta i en komposition efter segmenteringsaktiviteter.

Om du har konfigurerat en anslutning till Federated Audience Composition-målet kan du använda Enrichment-aktiviteten för att berika data som kommer från Adobe Experience Platform med attribut från din externa databas. [Lär dig hur du berikar Adobe Experience Platform-målgrupper med externa data](../../connections/destinations.md)

Anrikningsdata kan komma antingen:

* **Från samma arbetstabell** som den som är avsedd för din komposition:

  *Ange en grupp kunder som mål och lägg till fältet &quot;Födelsedatum&quot; i den aktuella arbetstabellen*.

* **Från en annan arbetstabell**:

  *Aktivera en grupp kunder och lägg till fälten Belopp och Produkttyp som kommer från tabellen Inköp*.

När anrikningsdata har lagts till i kompositionen kan de användas i aktiviteter som lagts till efter **anrikningsaktiviteten** för att segmentera kunder i distinkta grupper baserat på deras beteenden, inställningar och val.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Konfigurera anrikningsaktiviteten {#enrichment-configuration}

Så här konfigurerar du aktiviteten **Enrichment**:

1. Lägg till aktiviteter som **Skapa målgrupp** och **Kombinera** aktiviteter.
1. Lägg till en **anrikningsaktivitet**.

   ![](../assets/enrichment.png)

1. Om flera övergångar har konfigurerats i din komposition kan du använda fältet **[!UICONTROL Primary set]** för att definiera vilken övergång som ska användas som primär uppsättning för att utöka med data.

1. Klicka på **Lägg till anrikningsdata** och markera attributet som ska användas för att utöka data.

   ![](../assets/enrichment-add.png)

   >[!NOTE]
   >
   >Med knappen **Redigera uttryck** i attributmarkeringsskärmen kan du skapa avancerade uttryck för att välja attributet.

<!--PAS VU SUR INSTANCE: You can select two types of enrichment data: a single enrichment attribute from the target dimension, or a collection link. Each of these types is detailed in the examples below:

    * [Single enrichment attribute](#single-attribute)
    * [Collection lnk](#collection-link)-->

<!--
## Examples {#example}

### Single enrichment attribute {#single-attribute}

Here, we are just adding a single enrichment attribute, for example, the date of birth. Follow these steps:

1. Click inside the **Attribute** field.
1. Select a simple field from the schema, also known as targeting dimension, the date of birth in our example. 
1. Click **Confirm**.
-->
<!--### Collection link {#collection-link}

In this more complex use case, we will select a collection link which is a link with a 1-N cardinality between tables. Let's retrieve the three latest purchases that are less than 100$. For this you need to define:

* an enrichment attribute: the **Total amount** field
* the number of lines to retrieve: 3
* a filter: filter out items that are greater than 100$
* a sorting: descendant sorting on the **Order date** field. 

#### Add the attribute {#add-attribute}

This is where you select the collection link to use as enrichment data.

1. Click inside the **Attribute** field.
1. Click **Display advanced attributes**.
1. Select the **Total amount** field from the **Purchases** table. 

#### Define the collection settings{#collection-settings}

Then, define how the data is collected and the number of records to retrieve.

1. Select **Collect data** in the **Select how the data is collected** drop-down.
1. Type "3" in the **Lines to retrieve (Columns to create)** field. 

If you want, for example, to get the average amount of purchases for a customer, select **Aggregated data** instead, and select **Average** in the **Aggregate function** drop-down.

#### Define the filters{#collection-filters}

Here, we define the maximum value for the enrichment attribute. We filter out items that are greater than 100$. [Learn how to work with the query modeler](../../query/query-modeler-overview.md)

1. Click **Edit filters**.
1. Add the two following filters: **Total amount** exists AND **Total amount** is less than 100. The first one filters NULL values as they would appear as the greatest value.
1. Click **Confirm**.

#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.-->
