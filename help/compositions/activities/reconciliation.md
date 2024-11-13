---
audience: end-user
title: Använd avstämningsaktiviteten
description: Lär dig använda avstämningsaktiviteten
exl-id: 933c3cba-9120-4a93-a668-866fb65ee197
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Avstämning {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Avstämningsaktivitet"
>abstract="Med aktiviteten **Avstämning** kan du definiera länken mellan data i databasen och data i en arbetstabell."

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

Med aktiviteten **Avstämning** kan du definiera länken mellan data i databasen och data i en arbetstabell, till exempel data som lästs in från ett externt system.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

Det gör att du kan länka oidentifierade data till befintliga resurser. Avstämningsåtgärden innebär att de data som du ansluter redan finns i databasen. Om du till exempel vill stämma av inköpen, som visar vilken produkt som köpts, vid vilken tidpunkt, av vilken kund, osv., måste produkten och klienten redan finnas i databasen.

## Konfigurera avstämningsaktiviteten {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Välj det nya schemat som ska användas på data. Med ett schema, som också kallas måldimension, kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv. Som standard är dispositionsschemat valt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Avstämningsregler"
>abstract="Välj avstämningsregler som ska användas för dedupliceringen. Om du vill använda attribut markerar du alternativet **Enkla attribut** och väljer käll- och målfälten. Om du vill skapa ett eget avstämningsvillkor med frågemodelleraren väljer du alternativet **Avancerade avstämningsvillkor** ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Välj måldimension"
>abstract="Välj schemat, även kallat måldimension, för inkommande data som ska stämma av med."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Behåll ej avstämda data"
>abstract="Som standard behålls ej avstämda data i den utgående övergången och är tillgängliga i arbetstabellen för framtida bruk. Om du vill ta bort ej avstämda data inaktiverar du alternativet **Behåll ej avstämda data**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Avstämningsattribut"
>abstract="Markera det attribut som ska användas för att stämma av data och bekräfta."

Så här konfigurerar du aktiviteten **Avstämning**:

1. Lägg till en **avstämningsaktivitet** i din komposition.

1. Välj **Nytt schema**. Med ett schema, som också kallas måldimension, kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv.

1. Välj de fält som ska användas för avstämningen. Du kan använda ett eller flera avstämningskriterier.

   1. Om du vill använda attribut för att stämma av data markerar du alternativet **Enkla attribut** och klickar sedan på knappen **Lägg till regel** .
   1. Markera fälten **Source** och **Mål** för avstämningen. Fältet **Source**. Fältet **Mål** motsvarar fälten i det valda schemat.

      Data avstäms när källan och målet är lika. Markera till exempel fälten **E-post** för att ta bort dubbletter av profiler baserat på deras e-postadress.

      Om du vill lägga till ytterligare avstämningsvillkor klickar du på knappen **Lägg till regel** . Om flera kopplingsvillkor anges måste ALLA verifieras så att data kan länkas ihop.

      ![](../assets/reconciliation-rules.png)

   1. Om du vill använda andra attribut för att stämma av data väljer du alternativet **Avancerade avstämningsvillkor** och klickar sedan på knappen **Skapa villkor** . Du kan sedan skapa ett eget avstämningsvillkor med frågemodelleraren. [Lär dig arbeta med frågemodelleraren](../../query/query-modeler-overview.md)

      ![](../assets/reconciliation-advanced.png)

1. Du kan filtrera data så att de stäms av med knappen **Skapa filter** . Detta gör att du kan skapa ett anpassat villkor med hjälp av frågemodelleraren.

Som standard lagras ej avstämda data i den utgående övergången och är tillgängliga i arbetsboken för framtida bruk. Om du vill ta bort ej avstämda data inaktiverar du alternativet **Behåll ej avstämda data**.

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
