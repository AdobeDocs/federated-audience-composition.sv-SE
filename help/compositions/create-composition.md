---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---


# Skapa och konfigurera kompositionen {#create}

Det första steget för att skapa en komposition är att definiera dess etikett och konfigurera ytterligare inställningar om det behövs.

## Skapa kompositionen {#create-the-composition}

1. Gå till menyn **[!UICONTROL Audiences]** och välj fliken **[!UICONTROL Federated compositions]**.

1. Klicka på knappen **[!UICONTROL Create composition]**.

   ![](assets/composition-create.png)

1. I avsnittet **[!UICONTROL Properties]** anger du en etikett för kompositionen och klickar på **[!UICONTROL Create]**.

1. Dispositionsarbetsytan visas. Nu kan du konfigurera kompositionen genom att lägga till så många aktiviteter som behövs för att passa dina behov innan du kör den:

   * [Lär dig att samordna aktiviteter](#action-activities)
   * [Lär dig hur du startar och övervakar en komposition](#save)

## Konfigurera kompositionens inställningar {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Kompositionsegenskaper"
>abstract="Det här avsnittet innehåller generiska kompositionsegenskaper som också är tillgängliga när du skapar kompositionen."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Dispositionssegmentering"
>abstract="Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Du kan aktivera det här alternativet om du vill behålla arbetsregister för testning. Den får bara användas **endast** i utvecklings- eller mellanlagringsmiljöer. Den får aldrig kontrolleras i en produktionsmiljö."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Inställningar för felhantering"
>abstract="I det här avsnittet kan du definiera hur fel ska hanteras under körningen. Du kan välja att pausa processen, ignorera ett visst antal fel eller avbryta kompositionskörningen."

När du öppnar en komposition kan du komma åt avancerade inställningar som t.ex. gör att du kan definiera hur kompositionen ska fungera om fel uppstår.

Om du vill få tillgång till fler alternativ för kompositionen klickar du på knappen **[!UICONTROL Settings]** som finns i det övre avsnittet på skärmen där kompositionen skapas.

![](assets/composition-create-settings.png)

Tillgängliga inställningar är följande:

* **[!UICONTROL Label]**: Ändra kompositionens etikett.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Som standard behålls endast arbetsregister för den senaste körningen av kompositionen. Arbetstabeller från tidigare avrättningar rensas av en teknisk komposition som körs dagligen.

  Om det här alternativet är aktiverat behålls arbetsregister även efter att kompositionen har utförts. Du kan använda den i testsyfte och måste därför användas **endast** i utvecklings- eller staging-miljöer. Den får aldrig kontrolleras i en produktionskomposition.

* **[!UICONTROL Error management]**: Med det här alternativet kan du definiera de åtgärder som ska vidtas om en dispositionsaktivitet har fel. Det finns tre möjliga alternativ:

   * **[!UICONTROL Suspend the process]**: Kompositionen pausas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst kan du återuppta kompositionen med **[!UICONTROL Resume]**-knapparna.
   * **[!UICONTROL Ignore]**: Statusen för aktiviteten som utlöste felet ändras till **[!UICONTROL Failed]**, men dispositionen behåller statusen **[!UICONTROL Started]**.
   * **[!UICONTROL Abord the process]**: Kompositionen stoppas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst startar du om kompositionen med knappen **[!UICONTROL Start]**.

* **[!UICONTROL Consecutive errors]**: Ange antalet fel som kan ignoreras innan processen stoppas. När det här numret har nåtts ändras dispositionsstatusen till **[!UICONTROL Failed]**. Om värdet för det här fältet är 0 stoppas aldrig kompositionen oavsett antalet fel.
