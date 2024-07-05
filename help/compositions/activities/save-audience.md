---
audience: end-user
title: Använda aktiviteten Spara målgrupp
description: Lär dig hur du använder aktiviteten Spara målgrupper
source-git-commit: 6b7a0ae164bdb09b1f5fc067a13e304eec9c5201
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Spara målgrupp {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Spara en publik"
>abstract="Använd den här aktiviteten för att uppdatera en befintlig målgrupp eller skapa en ny målgrupp från populationen som beräknas uppströms i kompositionen. De målgrupper som skapas läggs till i listan över målgrupper och är tillgängliga via **Målgrupper** -menyn."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Generera utgående övergång"
>abstract="Använd det här alternativet om du vill lägga till en övergång efter **Spara målgrupper** aktivitet."

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

The **Spara målgrupper** Med -aktivitet kan du uppdatera en befintlig målgrupp eller skapa en ny målgrupp från populationen som beräknas uppströms i en komposition. De målgrupper som skapas läggs till i listan över programmålgrupper och blir tillgängliga via **Målgrupper** -menyn.

Denna verksamhet används främst för att få populationsgrupper att beräknas i samma sammansättning genom att de omvandlas till återanvändbara målgrupper. Koppla det till andra målinriktningsaktiviteter som **Bygg målgrupper** eller en **Kombinera** aktivitet.

## Konfigurera aktiviteten Spara målgrupp {#save-audience-configuration}

Följ de här stegen för att konfigurera **Spara målgrupper** aktivitet:

1. Lägg till en **Spara målgrupper** till din komposition.

   ![](../assets/save-audience.png)

1. Ange etiketten för målgruppen som ska skapas.

1. Klicka **Lägg till målgruppsmappning** välj sedan käll- och målgruppsfälten:

   * **Source Audience Field**:
   * **Målgruppsfält**:

   Upprepa åtgärden för att lägga till så många målgruppsmappningar som behövs.

1. Välj den primära identitet och det namnutrymme som ska användas för att identifiera målprofilerna i databasen:

   * **Primärt identitetsfält**: Markera det fält som ska användas för att identifiera profilerna. Till exempel dess e-postadress eller telefonnummer.
   * **Namnutrymme för identitet**: Välj det namnutrymme som ska användas för att identifiera profilerna, dvs. vilken typ av data som ska användas som identifieringsnyckel. Om e-postadressen till exempel har valts som primärt identitetsfält anger identitetsnamnutrymmet **E-post** ska vara markerat. Om den unika identifieraren är telefonnumret är identitetsnamnutrymmet **Telefon** ska vara markerat.

När kompositionen är klar sparas målgruppen i Adobe Experience Platform <!-- to check-->och som är tillgängliga i **Målgrupper** -menyn.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
