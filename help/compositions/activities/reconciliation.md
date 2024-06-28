---
audience: end-user
title: Använd avstämningsaktiviteten
description: Lär dig använda avstämningsaktiviteten
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 6%

---

# Avstämning {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Avstämningsaktivitet"
>abstract="The **Avstämning** kan du definiera länken mellan data i databasen och data i en arbetstabell."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Avstämningsmarkeringsfält"
>abstract="Avstämningsmarkeringsfält"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Avstämning skapa villkor"
>abstract="Avstämning skapa villkor"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Avstämning genererar komplementtal"
>abstract="Avstämning genererar komplementtal"

The **Avstämning** Med -aktivitet kan du definiera länken mellan data i databasen och data i en arbetstabell, till exempel data som lästs in från ett externt system.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

## Bästa praxis {#reconciliation-best-practices}

Med **Berikning** kan du definiera ytterligare data som ska bearbetas i kompositionen (du kan använda en **Berikning** aktivitet för att kombinera data från flera uppsättningar eller för att skapa länkar till en tillfällig resurs), **Avstämning** kan du länka oidentifierade data till befintliga resurser.

>[!NOTE]
>Avstämningsåtgärden innebär att data för de länkade dimensionerna redan finns i databasen.  Om du till exempel importerar en inköpsfil som visar vilken produkt som köptes vid en viss tidpunkt, av en viss klient och så vidare, så måste produkten och klienten redan finnas i databasen.

## Konfigurera avstämningsaktiviteten {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Måldimension"
>abstract="Välj den nya måldimensionen. Med en dimension kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv. Som standard är den aktuella måldimensionen markerad."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Avstämningsregler"
>abstract="Välj avstämningsregler som ska användas för dedupliceringen. Välj **Enkla attribut** och välj käll- och målfälten. Om du vill skapa ett eget avstämningsvillkor med frågemodelleraren väljer du **Avancerade avstämningsvillkor** alternativ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Välj måldimension"
>abstract="Välj måldimension för inkommande data som ska förenas med."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Behåll ej avstämda data"
>abstract="Som standard behålls ej avstämda data i den utgående övergången och är tillgängliga i arbetstabellen för framtida bruk. Om du vill ta bort ej avstämda data inaktiverar du **Behåll ej avstämda data** alternativ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Avstämningsattribut"
>abstract="Markera det attribut som ska användas för att avstämma data och bekräfta."

Följ de här stegen för att konfigurera **Avstämning** aktivitet:

1. Lägg till en **Avstämning** till din komposition. <!--This activity should be added following a transition containing a population whose targeting dimension does not directly come from Adobe Campaign. -->

1. Välj den nya måldimensionen. Med en dimension kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions).-->

1. Välj de fält som ska användas för avstämningen. Du kan använda ett eller flera avstämningskriterier.

   1. Om du vill använda attribut för att stämma av data väljer du **Enkla attribut** alternativ. The **Source** -fält visar de fält som är tillgängliga i indataövergången och som ska förenas. The **Mål** fältet motsvarar fälten i den valda måldimensionen. Data avstäms när källan och målet är lika. Välj till exempel **E-post** fält för att deduplicera profiler baserat på deras e-postadress.

      Om du vill lägga till ytterligare avstämningsvillkor klickar du på **Lägg till regel** -knappen. Om flera kopplingsvillkor anges måste ALLA verifieras så att data kan länkas ihop.

   <!--     ![](../assets/workflow-reconciliation-criteria.png)-->

   1. Om du vill använda andra attribut för att stämma av data väljer du **Avancerade avstämningsvillkor** alternativ. Du kan sedan skapa ett eget avstämningsvillkor med frågemodelleraren. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md).-->

1. Du kan använda **Skapa filter** -knappen. Detta gör att du kan skapa ett anpassat villkor med hjälp av frågemodelleraren. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

Som standard lagras ej avstämda data i den utgående övergången och är tillgängliga i arbetsboken för framtida bruk. Om du vill ta bort ej avstämda data inaktiverar du **Behåll ej avstämda data** alternativ.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
