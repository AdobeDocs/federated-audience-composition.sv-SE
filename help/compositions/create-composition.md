---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---


# Skapa och utföra en komposition {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="Egenskaper för arbetsflöde"
>abstract="På den här skärmen väljer du den mall som ska användas för att skapa arbetsflödet och anger en etikett. Expandera sektionen Ytterligare OPTIONS om du vill konfigurera fler inställningar, till exempel arbetsflödets interna namn, dess mapp, tidszon och övervakningsgrupp. Vi rekommenderar starkt att du väljer en grupp för ansvariga så att de får ett meddelande om ett fel inträffar."

## Skapa kompositionen {#create}

Så här skapar du en komposition:

1. Öppna **[!UICONTROL Audiences]** och väljer **[!UICONTROL Federated compositions]** -fliken.

1. Klicka på knappen **[!UICONTROL Create composition]**.

1. I **[!UICONTROL Properties]** anger du en etikett för montaget och klickar på **[!UICONTROL Create]**.

1. Dispositionsarbetsytan visas. Nu kan du konfigurera kompositionen genom att lägga till så många aktiviteter som behövs för att passa dina behov innan du kör den. Du kan också konfigurera ytterligare inställningar, till exempel kompositionens etikett eller alternativ som är relaterade till felhantering när kompositionen körs.

Läs mer i följande avsnitt:

* [Konfigurera kompositionens inställningar](#starting-audience)
* [Lägg till aktiviteter](#action-activities)
* [Utför kompositionen och övervaka dess körning](#save)

## Konfigurera kompositionens inställningar {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Kompositionsegenskaper"
>abstract="Det här avsnittet innehåller generiska kompositionsegenskaper som också är tillgängliga när du skapar kompositionen."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Dispositionssegmentering"
>abstract="Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Du kan aktivera det här alternativet om du vill behålla arbetsregister för testning. Det måste användas **endast** i utvecklings- eller stagingmiljöer. Den får aldrig kontrolleras i en produktionsmiljö."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Inställningar för felhantering"
>abstract="I det här avsnittet kan du definiera hur fel ska hanteras under körningen. Du kan välja att pausa processen, ignorera ett visst antal fel eller avbryta kompositionskörningen."

Klicka på **Inställningar** för att få tillgång till fler alternativ för kompositionen:

* **[!UICONTROL Label]**: Ändra kompositionens etikett.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Som standard behålls endast arbetstabellerna för den senaste körningen av kompositionen. Arbetstabeller från tidigare körningar rensas av ett tekniskt arbetsflöde, som körs dagligen.

  Om det här alternativet är aktiverat behålls arbetsregister även efter att kompositionen har utförts. Du kan använda den i testsyfte och måste därför användas **endast** i utvecklings- eller stagingmiljöer. Den får aldrig checkas in i ett produktionsarbetsflöde.

* **[!UICONTROL Error management]**: I det här avsnittet kan du definiera vilka åtgärder som ska vidtas om en dispositionsaktivitet har fel. Det finns tre möjliga alternativ:

   * **[!UICONTROL Suspend the process]**: Kompositionen pausas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst kan du återuppta kompositionen med **[!UICONTROL Resume]** knappar.
   * **[!UICONTROL Ignore]**: Status för den aktivitet som utlöste felet ändras till **[!UICONTROL Failed]**, men kompositionen behåller **[!UICONTROL Started]** status.
   * **[!UICONTROL Abord the process]**: Kompositionen stoppas automatiskt och dess status ändras till **[!UICONTROL Failed]**. När problemet är löst startar du om kompositionen med **[!UICONTROL Start]** -knappen.

* **[!UICONTROL Consecutive errors]**: Ange antalet fel som kan ignoreras innan processen stoppas. När det här talet har nåtts ändras dispositionsstatusen till **[!UICONTROL Failed]**. Om värdet för det här fältet är 0 stoppas aldrig kompositionen oavsett antalet fel.

## Lägg till aktiviteter {#activities}

Med arbetsytan kan du konfigurera så att du kan lägga till så många aktiviteter som behövs i kompositionen som passar dina behov.

Det gör du genom att klicka på plusknappen (+) på kompositionsbanan och sedan lägga till önskad aktivitet. Den högra rutan öppnas så att du kan konfigurera den nyligen tillagda aktiviteten. [Läs mer om aktiviteterna i kompositioner och hur du konfigurerar dem](../compositions/activities/about-activities.md)

Om du vill ta bort en aktivitet från arbetsytan markerar du den och klickar på knappen Ta bort i den högra rutan. Om aktiviteten som du vill ta bort är överordnad andra aktiviteter i kompositionen visas ett meddelande, som du kan använda för att ange om du bara vill ta bort den markerade aktiviteten eller alla dess underordnade aktiviteter.

## Utför kompositionen {#execute}

Klicka på **[!UICONTROL Start]** för att genomföra och spara målgrupperna i Adobe Experience Platform. &quot;Du kan övervaka arbetsflödets körning med **Loggar** -knappen. Det finns tre flikar som hjälper dig att övervaka körningen:

* **[!UICONTROL Logs]**:
* **[!UICONTROL Tasks]**:
* **[!UICONTROL Variables]**:
