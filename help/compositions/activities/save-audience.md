---
audience: end-user
title: Använda aktiviteten Spara målgrupp
description: Lär dig hur du använder aktiviteten Spara målgrupper
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: 7429577d99d2f163e7084db056005fe641d1bcf3
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Spara målgrupp {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Spara en publik"
>abstract="Använd den här aktiviteten för att skapa en ny målgrupp från populationen som beräknas uppströms i kompositionen. De målgrupper som skapas läggs till i listan över målgrupper och är tillgängliga via menyn **Publiker** ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Generera utgående övergång"
>abstract="Använd det här alternativet om du vill lägga till en övergång efter aktiviteten **Spara målgrupp**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Primärt identitetsfält"
>abstract="Välj den primära identitet som ska användas för profiler."
>additional-url="https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Läs mer i Experience Platform-dokumentationen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Namnutrymme för identitet"
>abstract="Välj det namnutrymme som ska användas för profiler."
>additional-url="https://experienceleague.adobe.com/sv/docs/experience-platform/identity/features/namespaces" text="Läs mer i Experience Platform-dokumentationen"

Med aktiviteten **[!UICONTROL Save audience]** kan du skapa en ny målgrupp från populationen som beräknas uppströms i en komposition. De målgrupper som skapas läggs till i listan över Adobe Experience Platform-målgrupper och blir tillgängliga via menyn **Publiker** . [Lär dig arbeta med målgrupper](../../start/audiences.md)

Denna verksamhet används främst för att få populationsgrupper att beräknas i samma sammansättning genom att de omvandlas till återanvändbara målgrupper. Koppla det till andra målinriktningsaktiviteter som **Skapa målgrupp** eller en **Kombinera**-aktivitet.

Aktiviteten **[!UICONTROL Save Audience]** genererar ett nytt målgruppsschema och associerad datauppsättning, som kan innehålla personligt identifierbar information (PII) eller skyddad hälsoinformation (PHI). När målgruppen har skapats bör du samarbeta med administratören för att försäkra dig om att rätt etiketter för datastyrning används i enlighet med organisationens datapolicyer. Mer information om hur du använder dataanvändningsetiketter finns i användarhandboken för [dataanvändningsetiketter](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/labels/user-guide).

## Konfigurera aktiviteten Spara målgrupp {#save-audience-configuration}

Så här konfigurerar du aktiviteten **Spara målgrupp**:

1. Lägg till en **Spara målgruppsaktivitet** i kompositionen.

   ![](../assets/save-audience.png)

1. Ange etiketten för målgruppen som ska skapas.

   >[!IMPORTANT]
   >
   >Målgruppsetiketten måste vara unik i den aktuella sandlådan. Det kan inte vara samma etikett som någon befintlig målgrupp.

1. Använd delen Målgruppsmappningar för att markera de fält du vill ta med den nya målgruppen. Det gör du genom att klicka på **Lägg till målgruppsmappning** och sedan välja käll- och målmålgruppsfälten.

   Upprepa åtgärden för att lägga till så många målgruppsmappningar som behövs.

1. Välj den primära identitet och det namnutrymme som ska användas för att identifiera målprofilerna i databasen:

   * **Primärt identitetsfält**: Markera det fält som ska användas för att identifiera profilerna. Till exempel dess e-postadress eller telefonnummer.
   * **Identitetsnamnrymd**: Välj det namnutrymme som ska användas för att identifiera profilerna, dvs. den typ av data som ska användas som identifieringsnyckel. Om e-postadressen till exempel har valts som primärt identitetsfält bör identitetsnamnområdet **E-postadress** väljas. Om den unika identifieraren är telefonnumret bör identitetsnamnområdet **Telefon** väljas.

## Nå ut till er målgrupp i Adobe Experience Platform {#access-audience}

När kompositionen är klar sparas målgruppen i Adobe Experience Platform som en extern målgrupp och finns tillgänglig i Adobe Real-Time CDP och/eller Adobe Journey Optimizer i Audience Portal. Mer information om Audience Portal finns i [Översikt över Audience Portal](https://experienceleague.adobe.com/sv/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

Den skapade målgruppen innehåller alla fält som har markerats i avsnittet Målgruppsmappningar. Du kan rikta in den här målgruppen i Journey Optimizer eller aktivera den på alla målplatser som stöds av Adobe Experience Platform.

[Läs mer i Adobe Experience Platform-dokumentationen](https://experienceleague.adobe.com/sv/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
