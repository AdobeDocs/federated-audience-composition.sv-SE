---
audience: end-user
title: Create compositions
description: Learn how to create compositions
badge: label="Limited availability" type="Informative"
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: bd3223a77f490a43487e21662d8f766d4f9b06fc
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Create &amp; configure the composition {#create}

The first step to create a composition is to define its label and configure additional settings if needed.

## Skapa kompositionen {#create-the-composition}

1. Gå till menyn **[!UICONTROL Audiences]** och välj fliken **[!UICONTROL Federated compositions]**.

1. Klicka på knappen **[!UICONTROL Create composition]**.

   ![](assets/composition-create.png)

1. I avsnittet **[!UICONTROL Properties]** anger du en etikett för kompositionen och väljer en datamodell. Endast scheman som är kopplade till den här datamodellen är tillgängliga i dispositionens aktiviteter.

   ![](assets/composition-select-schema.png)

1. Klicka på **[!UICONTROL Create]**. Dispositionsarbetsytan visas. Nu kan du konfigurera kompositionen genom att lägga till så många aktiviteter som behövs för att passa dina behov innan du kör den:

   * [Lär dig att samordna aktiviteter](orchestrate-activities.md)
   * [](start-monitor-composition.md)

## Configure the composition&#39;s settings {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Composition properties"
>abstract="Det här avsnittet innehåller generiska kompositionsegenskaper som också är tillgängliga när du skapar kompositionen."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Dispositionssegmentering"
>abstract="Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Du kan aktivera det här alternativet om du vill behålla arbetsregister för testning. Den får bara användas **endast** i utvecklings- eller mellanlagringsmiljöer. Den får aldrig kontrolleras i en produktionsmiljö."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Inställningar för felhantering"
>abstract="I det här avsnittet kan du definiera hur fel ska hanteras under körningen. Du kan välja att pausa processen, ignorera ett visst antal fel eller avbryta kompositionskörningen."

When accessing a composition, you can access advanced settings that allow you, for example, to define how the composition should behave in case of error. **[!UICONTROL Settings]**

![](assets/composition-create-settings.png)

Available settings are as follows:

* **[!UICONTROL Label]**

* **[!UICONTROL Keep the result of interim populations between two executions]** Arbetstabeller från tidigare avrättningar rensas av en teknisk komposition som körs dagligen.

  Om det här alternativet är aktiverat behålls arbetsregister även efter att kompositionen har utförts. Du kan använda den i testsyfte och måste därför användas **endast** i utvecklings- eller staging-miljöer. Den får aldrig kontrolleras i en produktionskomposition.

* **[!UICONTROL Error management]**: Med det här alternativet kan du definiera de åtgärder som ska vidtas om en dispositionsaktivitet har fel. Det finns tre möjliga alternativ:

   * **[!UICONTROL Suspend the process]**: Kompositionen pausas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst kan du återuppta kompositionen med **[!UICONTROL Resume]**-knapparna.
   * **[!UICONTROL Ignore]**: Statusen för aktiviteten som utlöste felet ändras till **[!UICONTROL Failed]**, men dispositionen behåller statusen **[!UICONTROL Started]**.
   * **[!UICONTROL Abort the process]****[!UICONTROL Failed]** **[!UICONTROL Start]**

* **[!UICONTROL Consecutive errors]** **[!UICONTROL Failed]** If the value of this field is 0, the composition will never be stopped regardless of the number of errors.
