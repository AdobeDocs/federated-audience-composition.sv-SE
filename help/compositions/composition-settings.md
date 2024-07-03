---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---


# Konfigurera kompositionens inställningar {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Kompositionsegenskaper"
>abstract="Det här avsnittet innehåller generiska kompositionsegenskaper som också är tillgängliga när du skapar kompositionen."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Dispositionssegmentering"
>abstract="Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Du kan aktivera det här alternativet om du vill behålla arbetsregister för testning. Det måste användas **endast** i utvecklings- eller stagingmiljöer. Den får aldrig kontrolleras i en produktionsmiljö."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Inställningar för felhantering"
>abstract="I det här avsnittet kan du definiera hur fel ska hanteras under körningen. Du kan välja att pausa processen, ignorera ett visst antal fel eller avbryta kompositionskörningen."

När du öppnar en komposition kan du komma åt avancerade inställningar som t.ex. gör att du kan definiera hur kompositionen ska fungera om fel uppstår, eller hantera den fördröjning efter vilken kompositionshistoriken ska rensas.

Om du vill visa fler alternativ för kompositionen klickar du på **Inställningar** ovanför arbetsytan.

![](assets/composition-create-settings.png)

Tillgängliga inställningar är följande:

* **[!UICONTROL Label]**: Ändra kompositionens etikett.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Arbetstabeller från tidigare avrättningar rensas av en teknisk komposition som körs dagligen.

  Om det här alternativet är aktiverat behålls arbetsregister även efter att kompositionen har utförts. Du kan använda den i testsyfte och måste därför användas **endast** i utvecklings- eller stagingmiljöer. Den får aldrig kontrolleras i en produktionskomposition.

* **[!UICONTROL Error management]**: I det här avsnittet kan du definiera vilka åtgärder som ska vidtas om en dispositionsaktivitet har fel. Det finns tre möjliga alternativ:

   * **[!UICONTROL Suspend the process]**: Kompositionen pausas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst kan du återuppta kompositionen med **[!UICONTROL Resume]** knappar.
   * **[!UICONTROL Ignore]**: Status för den aktivitet som utlöste felet ändras till **[!UICONTROL Failed]**, men kompositionen behåller **[!UICONTROL Started]** status.
   * **[!UICONTROL Abord the process]**: Kompositionen stoppas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst startar du om kompositionen med **[!UICONTROL Start]** -knappen.

* **[!UICONTROL Consecutive errors]**: Ange antalet fel som kan ignoreras innan processen stoppas. När det här talet har nåtts ändras dispositionsstatusen till **[!UICONTROL Failed]**. Om värdet för det här fältet är 0 stoppas aldrig kompositionen oavsett antalet fel.
