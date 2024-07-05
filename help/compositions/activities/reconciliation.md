---
audience: end-user
title: Använd avstämningsaktiviteten
description: Lär dig använda avstämningsaktiviteten
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

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

The **Avstämning** kan du länka oidentifierade data till befintliga resurser. Avstämningsåtgärden innebär att de data som du ansluter redan finns i databasen. Om du t.ex. vill avstämma inköpsinformation som visar vilken produkt som köptes, vid vilken tidpunkt, av vilken klient, osv., måste produkten och klienten redan finnas i databasen.

## Konfigurera avstämningsaktiviteten {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Välj det nya schemat som ska användas på data. Med ett schema, som också kallas måldimension, kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv. Som standard är dispositionsschemat valt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Avstämningsregler"
>abstract="Välj avstämningsregler som ska användas för dedupliceringen. Välj **Enkla attribut** och välj käll- och målfälten. Om du vill skapa ett eget avstämningsvillkor med frågemodelleraren väljer du **Avancerade avstämningsvillkor** alternativ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Välj måldimension"
>abstract="Välj schemat, även kallat måldimension, för inkommande data som ska stämma av med."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Behåll ej avstämda data"
>abstract="Som standard behålls ej avstämda data i den utgående övergången och är tillgängliga i arbetstabellen för framtida bruk. Om du vill ta bort ej avstämda data inaktiverar du **Behåll ej avstämda data** alternativ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Avstämningsattribut"
>abstract="Markera det attribut som ska användas för att avstämma data och bekräfta."

Följ de här stegen för att konfigurera **Avstämning** aktivitet:

1. Lägg till en **Avstämning** till din komposition.

1. Välj **Nytt schema**. Med ett schema, som också kallas måldimension, kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv.

1. Välj de fält som ska användas för avstämningen. Du kan använda ett eller flera avstämningskriterier.

   1. Om du vill använda attribut för att stämma av data väljer du **Enkla attribut** sedan klickar du på **Lägg till regel** -knappen.
   1. Välj **Source** och **Mål** fält för avstämningen. The **Source** fält. The **Mål** fältet motsvarar fälten i det valda schemat.

      Data avstäms när källan och målet är lika. Välj till exempel **E-post** fält för att deduplicera profiler baserat på deras e-postadress.

      Om du vill lägga till ytterligare avstämningsvillkor klickar du på **Lägg till regel** -knappen. Om flera kopplingsvillkor anges måste ALLA verifieras så att data kan länkas ihop.

      ![](../assets/reconciliation-rules.png)

   1. Om du vill använda andra attribut för att stämma av data väljer du **Avancerade avstämningsvillkor** sedan klickar du på **Skapa villkor** -knappen. Du kan sedan skapa ett eget avstämningsvillkor med frågemodelleraren.

      ![](../assets/reconciliation-advanced.png)

1. Du kan använda **Skapa filter** -knappen. Detta gör att du kan skapa ett anpassat villkor med hjälp av frågemodelleraren.

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
