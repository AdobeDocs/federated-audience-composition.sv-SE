---
audience: end-user
title: Använda aktiviteten Spara målgrupp
description: Lär dig hur du använder aktiviteten Spara målgrupper
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Spara målgrupp {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Spara en publik"
>abstract="Använd den här aktiviteten för att uppdatera en befintlig målgrupp eller skapa en ny målgrupp från populationen som beräknas uppströms i kompositionen. De målgrupper som skapas läggs till i listan över målgrupper och är tillgängliga via menyn **Publiker** ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Generera utgående övergång"
>abstract="Använd det här alternativet om du vill lägga till en övergång efter aktiviteten **Spara målgrupp**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Primärt identitetsfält"
>abstract="Välj den primära identitet som ska användas för profiler."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Läs mer i dokumentationen för Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Namnutrymme för identitet"
>abstract="Välj det namnutrymme som ska användas för profiler."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces" text="Läs mer i dokumentationen för Experience Platform"

Med aktiviteten **Spara målgrupp** kan du uppdatera en befintlig målgrupp eller skapa en ny målgrupp utifrån den population som beräknas uppströms i en komposition. De målgrupper som skapas läggs till i listan över programmålgrupper och blir tillgängliga via menyn **Publiker** .

Denna verksamhet används främst för att få populationsgrupper att beräknas i samma sammansättning genom att de omvandlas till återanvändbara målgrupper. Koppla det till andra målinriktningsaktiviteter som **Skapa målgrupp** eller en **Kombinera**-aktivitet.

## Konfigurera aktiviteten Spara målgrupp {#save-audience-configuration}

Så här konfigurerar du aktiviteten **Spara målgrupp**:

1. Lägg till en **Spara målgruppsaktivitet** i kompositionen.

   ![](../assets/save-audience.png)

1. Ange etiketten för målgruppen som ska skapas.

1. Klicka på **Lägg till målgruppsmappning** och välj käll- och målmålgruppsfälten:

   * **Source målgruppsfält**:
   * **Målgruppsfält**:

   Upprepa åtgärden för att lägga till så många målgruppsmappningar som behövs.

1. Välj den primära identitet och det namnutrymme som ska användas för att identifiera målprofilerna i databasen:

   * **Primärt identitetsfält**: Markera det fält som ska användas för att identifiera profilerna. Till exempel dess e-postadress eller telefonnummer.
   * **Identitetsnamnrymd**: Välj det namnutrymme som ska användas för att identifiera profilerna, dvs. den typ av data som ska användas som identifieringsnyckel. Om e-postadressen till exempel har valts som primärt identitetsfält bör identitetsnamnområdet **E-postadress** väljas. Om den unika identifieraren är telefonnumret bör identitetsnamnområdet **Telefon** väljas.

När kompositionen har körts sparas den slutliga publiken i Adobe Experience Platform <!-- to check--> och blir tillgänglig på menyn **Publiker** .

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
