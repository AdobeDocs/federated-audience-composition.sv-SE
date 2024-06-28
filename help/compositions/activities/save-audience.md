---
audience: end-user
title: Använda aktiviteten Spara målgrupp
description: Lär dig hur du använder gaffelaktiviteten
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

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

1. I **Läge** väljer du den åtgärd du vill utföra:

   * **Skapa eller uppdatera en befintlig målgrupp**: definiera en **Målgruppsetikett**. Om målgruppen redan finns uppdateras den, annars skapas en ny målgrupp.

   * **Uppdatera en befintlig målgrupp**: välj **Målgrupp** som du vill uppdatera bland de befintliga målgrupperna.

1. Välj **Uppdateringsläge** som ska gälla för befintliga målgrupper:

   * **Ersätt målgruppsinnehåll med nya data**: allt målgruppsinnehåll ersätts. Gammal data går förlorad.  Endast data från den inkommande övergången av målgruppsaktiviteten för att spara sparas. Med det här alternativet raderas målgruppstypen och målgruppsdimensionen för den uppdaterade målgruppen.

   * **Komplett målgrupp med nya data**: det gamla målgruppsinnehållet behålls och data från den sparade målgruppsaktivitetens inkommande övergång läggs till i det.

1. Kontrollera **Generera en utgående övergång** om du vill lägga till en övergång efter **Spara målgrupper** aktivitet.

Innehållet i den sparade målgruppen är sedan tillgängligt i detaljvyn för målgruppen, som du kommer åt via **Målgrupper** -menyn. Kolumnerna som är tillgängliga från den här vyn motsvarar kolumnerna för den inkommande övergången i **Spara målgrupper** aktivitet.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
