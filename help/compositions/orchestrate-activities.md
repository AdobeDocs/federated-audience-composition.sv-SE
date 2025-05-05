---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
exl-id: 7b9acfc0-99b6-4f83-b774-3652c811868c
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Orchestrate-dispositionsaktiviteter {#activities}

När du har skapat en komposition kan du börja organisera de olika uppgifter som ska utföras. För att göra detta finns en visuell arbetsyta som gör att du kan skapa ett målgruppsdiagram. I det här diagrammet kan du lägga till olika aktiviteter och koppla dem i en sekventiell ordning.

## Lägg till aktiviteter {#add}

I det här skedet av konfigurationen visas diagrammet med en startikon som representerar början av kompositionen. Om du vill lägga till din första aktivitet klickar du på knappen **+** som är ansluten till startikonen.

En lista över aktiviteter som kan läggas till i diagrammet visas. Vilka aktiviteter som är tillgängliga beror på var du befinner dig i dispositionsdiagrammet. När du till exempel lägger till din första aktivitet kan du starta dispositionen genom att rikta in dig på en målgrupp, dela dispositionssökvägen, ange inställningar för en schemaläggare för att fördröja dispositionskörningen eller ange en **Vänta** -aktivitet för att fördröja kompositionskörningen. Efter en **Bygg målgrupp** kan du å andra sidan förfina ditt mål med riktade aktiviteter eller organisera dispositionsprocessen med flödeskontrollaktiviteter.

När en aktivitet har lagts till i diagrammet visas en höger ruta där du kan konfigurera den nyligen tillagda aktiviteten med specifika inställningar. Detaljerad information om hur du konfigurerar varje aktivitet finns i [det här avsnittet](activities/about-activities.md).

![](assets/composition-create-add.png)

Upprepa den här processen om du vill lägga till så många aktiviteter som du vill, beroende på vilka uppgifter du vill att kompositionen ska utföra. Observera att du även kan infoga en ny aktivitet mellan två aktiviteter. Det gör du genom att klicka på knappen **+** för övergången mellan aktiviteterna, markera önskad aktivitet och konfigurera den i den högra rutan.

>[!TIP]
>
>Du kan anpassa namnet på övergångarna mellan varje aktivitet. Det gör du genom att markera övergången och ändra dess etikett i den högra rutan.

## Verktygsfältet Arbetsyta {#toolbar}

Verktygsfältet som finns i det övre högra hörnet av arbetsytan innehåller alternativ för att enkelt ändra aktiviteterna och navigera på arbetsytan.

![](assets/canvas-toolbar.png)

Tillgängliga åtgärder är:

* **[!UICONTROL Multiple selection]**: Markera flera aktiviteter om du vill ta bort alla samtidigt eller kopiera och klistra in dem. Se [det här avsnittet](#copy).
* **[!UICONTROL Rotate]**: Växla arbetsytan lodrätt.
* **[!UICONTROL Fit to screen]**: Anpassa arbetsytans zoomnivå till skärmen.
* **[!UICONTROL Zoom out]** / **[!UICONTROL Zoom in]**: Zooma ut eller in på arbetsytan.
* **[!UICONTROL Display map]**: Öppnar en ögonblicksbild av arbetsytan som visar att du finns.

## Hantera aktiviteter {#manage}

När du lägger till aktiviteter är åtgärdsknappar tillgängliga i egenskapsrutan, vilket gör att du kan utföra flera åtgärder.

![](assets/activity-actions.png)

Du kan:

* **[!UICONTROL Delete]** aktiviteten från arbetsytan.
* **[!UICONTROL Disable]/[!UICONTROL Enable]** aktiviteten. När kompositionen körs utförs inte inaktiverade aktiviteter och följande aktiviteter på samma sökväg och kompositionen stoppas.
* **[!UICONTROL Pause]/[!UICONTROL Resume]** aktiviteten. När kompositionen körs pausas den vid den pausade aktiviteten. Motsvarande uppgift och alla som följer den i samma sökväg körs inte.
* **[!UICONTROL Copy]** aktiviteten att klistra in den på en annan plats i kompositionen. Det gör du genom att klicka på knappen **+** för en övergång och välja **[!UICONTROL Paste X activity]**. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Konfigurera **[!UICONTROL Execution options]** för den valda aktiviteten. Expandera avsnittet nedan om du vill veta mer om de tillgängliga alternativen.

  +++Tillgängliga körningsalternativ

  I avsnittet **[!UICONTROL Properties]** kan du konfigurera allmänna inställningar för aktivitetens körning:

   * **[!UICONTROL Execution]**: Definiera åtgärden som ska utföras när programmet startas.
   * **[!UICONTROL Maximum execution duration]**: Ange en varaktighet som 30s eller 1h. Om aktiviteten inte är klar efter att den angivna tiden har gått ut utlöses en varning. Detta påverkar inte hur kompositionen fungerar.
   * **[!UICONTROL Time zone]**: Välj aktivitetens tidszon. Med Federated Audience Composition kan du hantera tidsskillnader mellan flera länder i samma instans. Inställningen som används konfigureras när instansen skapas.
   * **[!UICONTROL Affinity]**: Tvinga kompositionsaktiviteten att köras på en viss dator. För att kunna göra detta måste du ange en eller flera tillhörigheter för aktiviteten i fråga.
   * **[!UICONTROL Behavior]**: Definiera proceduren som ska följas om asynkrona uppgifter används.

  I avsnittet **[!UICONTROL Error management]** kan du ange vilken åtgärd som ska utföras om aktiviteten stöter på ett fel.

  I avsnittet **[!UICONTROL Initialization script]** kan du initiera variabler eller ändra aktivitetsegenskaper. Klicka på knappen **[!UICONTROL Edit code]** och skriv det kodfragment som ska köras. Skriptet anropas när aktiviteten körs.

  +++

* Åtkomst till aktivitetens **loggar och uppgifter**.
