---
audience: end-user
title: Använda aktiviteten Kombinera
description: Lär dig använda aktiviteten Kombinera
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 12%

---


# Kombinera {#combine}

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Kombinera aktivitet"
>abstract="The **Kombinera** kan du segmentera den inkommande populationen. Du kan alltså kombinera flera populationer, exkludera delar av dem eller bara behålla data som är gemensamma för flera mål."

The **Kombinera** kan du segmentera den inkommande populationen. Du kan alltså kombinera flera populationer, utesluta en del av dem eller bara behålla data som är gemensamma för flera mål.

The **Kombinera** kan placeras efter andra aktiviteter, men inte i början av kompositionen. Alla aktiviteter kan placeras efter **Kombinera**.

## Konfigurera Kombinera-aktiviteten {#combine-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Sammanfogningsalternativ för skärningar"
>abstract="The **skärningspunkt** gör att du bara kan behålla de element som är gemensamma för de olika inkommande populationerna i aktiviteten. I **Uppsättningar att förena** markerar du alla tidigare aktiviteter du vill gå med i."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Alternativ för uteslutningssammanslagning"
>abstract="The **exkludering** gör att du kan utesluta element från en population enligt vissa kriterier. I **Uppsättningar att förena** markerar du alla tidigare aktiviteter du vill gå med i."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Välj segmenteringstyp"
>abstract="Välj hur du vill kombinera målgrupper: union, skärning eller uteslutning."

Följ de här vanliga stegen för att börja konfigurera **Kombinera** aktivitet:

1. Lägg till flera aktiviteter för att bilda minst två olika körningsgrenar.

1. Lägg till en **Kombinera** verksamhet till någon av de tidigare filialerna.

1. Välj segmenteringstyp: [Union](#union), [Skärningspunkt](#intersection) eller [Uteslutning](#exclusion)och klicka **Fortsätt**.

   ![](../assets/combine.png)

1. I **Uppsättningar att förena** markerar du alla tidigare aktiviteter som du vill ansluta till.

## Sammanslutning {#combine-union}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Avstämningsalternativ för skärningar"
>abstract="Välj avstämningstypen för att definiera hur dubbletter hanteras."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Avstämningsalternativ"
>abstract="Välj **Avstämningstyp** för att definiera hur dubbletter ska hanteras."

I **Kombinera** -aktivitet kan du konfigurera en **Union**.

![](../assets/combine-union.png)

För detta måste du välja **Avstämningstyp** för att definiera hur dubbletter hanteras:

* **Endast tangenter**: det här är standardläget. Aktiviteten behåller endast ett element när element från olika inkommande övergångar har samma nyckel.  Detta alternativ kan endast användas om de inkommande populationerna är homogena.
* **En markering med kolumner**: välj det här alternativet för att definiera listan med kolumner som datavstämningen ska användas på. Du måste först markera den primära uppsättningen (som innehåller källdata) och sedan de kolumner som ska användas för kopplingen.

## Skärningspunkt {#combine-intersection}

I **Kombinera** -aktivitet kan du konfigurera en **Skärningspunkt**.

![](../assets/combine-intersection.png)

För detta följer du de extra stegen nedan:

1. Välj **Avstämningstyp** för att definiera hur dubbletter hanteras. Se [Union](#union) -avsnitt.
1. Du kan kontrollera **Generera komplement** om du vill bearbeta den återstående populationen. Komplementet ska innehålla en kombination av resultaten av alla inkommande aktiviteter minus skärningspunkten. En ytterligare utgående övergång läggs sedan till i aktiviteten.

## Uteslutning {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Uteslutningsregler"
>abstract="Vid behov kan du ändra inkommande tabeller. Om du vill utesluta ett mål från ett annat schema, som också kallas måldimension, måste det här målet återställas till samma schema som huvudmålet. Det gör du genom att klicka **Lägg till en regel** i E **exkluderingsregler** och ange villkoren för schemaändring. Datavstämning utförs antingen via ett attribut eller en koppling."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Markera uppsättningar som ska kombineras"
>abstract="I **Uppsättningar att förena** väljer du **Primär uppsättning** från inkommande övergångar. Detta är den uppsättning från vilken element utesluts. De andra uppsättningarna matchar element innan de utesluts från den primära uppsättningen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Uteslutningsregler"
>abstract="Vid behov kan du ändra inkommande tabeller. Om du vill utesluta ett mål från ett annat schema, som också kallas måldimension, måste det här målet återställas till samma schema som huvudmålet. Det gör du genom att klicka **Lägg till en regel** i **Uteslutningsregler** och ange villkoren för schemaändring. Datavstämning utförs antingen via ett attribut eller en koppling."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Kombinera skapa komplementfärger"
>abstract="Växla på **Generera komplement** möjlighet att bearbeta den återstående populationen i en ytterligare övergång."

I **Kombinera** -aktivitet kan du konfigurera en **Uteslutning**.

![](../assets/combine-exclusion.png)

För detta behöver du följa de extra stegen nedan:

1. I **Uppsättningar att förena** väljer du **Primär uppsättning** från inkommande övergångar. Detta är den uppsättning från vilken element utesluts. De andra uppsättningarna matchar element innan de utesluts från den primära uppsättningen.

1. Vid behov kan du ändra inkommande tabeller. Om du vill utesluta ett mål från ett annat schema måste det här målet återställas till samma schema som huvudmålet. Det gör du genom att klicka **Lägg till en regel** i **Uteslutningsregler** och ange villkoren för schemaändring. Datavstämning utförs antingen via ett attribut eller en koppling. <!-- pas compris-->
1. Du kan kontrollera **Generera slutförande** om du vill bearbeta den återstående populationen. Se [Skärningspunkt](#intersection) -avsnitt.

<!--
## Examples{#combine-examples}

In the following example, we are using a **Combine** activity and we add a **union** to retrieves all the profiles of the two queries: persons between 18 and 27 years old and persons between 34 and 40 years old.

![](../assets/workflow-union-example.png)

The following example shows the **intersection** between two query activities. It is being used here to retrieve profiles who are between 18 to 27 years old and whose email address has been provided.

![](../assets/workflow-intersection-example.png)

The following **exclusion** example shows two queries configured to filter profiles who are between 18 and 27 years old and have an Adobe email domain. The profiles with an Adobe email domain are then excluded from the first set. 

![](../assets/workflow-exclusion-example.png)
-->
