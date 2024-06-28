---
audience: end-user
title: Kom igång med kompositioner
description: Lär dig hur du börjar med kompositioner
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Kom igång med kompositioner {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Kompositionsegenskaper"
>abstract="Det här avsnittet innehåller generiska kompositionsegenskaper som också är tillgängliga när du skapar kompositionen."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Dispositionssegmentering"
>abstract="Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Du kan aktivera det här alternativet om du vill behålla arbetsregister för testning. Det måste användas **endast** i utvecklings- eller stagingmiljöer. Den får aldrig kontrolleras i en produktionsmiljö."




## Vad är en komposition? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Kompositioner"
>abstract="På den här skärmen kan du komma åt den fullständiga listan med kompositioner, kontrollera deras aktuella status, senaste/nästa körningsdatum och skapa en ny komposition."


## Inställningar för felhantering  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Inställningar för felhantering"
>abstract="I det här avsnittet kan du definiera hur fel ska hanteras under körningen. Du kan välja att pausa processen, ignorera ett visst antal fel eller avbryta kompositionskörningen."

* **[!UICONTROL Error management]**: I det här fältet kan du definiera vilka åtgärder som ska vidtas om en dispositionsaktivitet har fel.
Det finns tre möjliga alternativ:

   * **[!UICONTROL Suspend the process]**: Kompositionen pausas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst kan du återuppta kompositionen med **[!UICONTROL Resume]** knappar.
   * **[!UICONTROL Ignore]**: Status för den aktivitet som utlöste felet ändras till **[!UICONTROL Failed]**, men kompositionen behåller **[!UICONTROL Started]** status.
   * **[!UICONTROL Abord the process]**: Kompositionen stoppas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst startar du om kompositionen med **[!UICONTROL Start]** -knappen.

* **[!UICONTROL Consecutive errors]**: Det här fältet blir tillgängligt när **[!UICONTROL Ignore]** värdet är markerat i **[!UICONTROL In case of errors]** fält. Du kan ange antalet fel som kan ignoreras innan processen stoppas. När det här talet har nåtts ändras dispositionsstatusen till **[!UICONTROL Failed]**. Om värdet för det här fältet är 0 stoppas aldrig kompositionen oavsett antalet fel.
