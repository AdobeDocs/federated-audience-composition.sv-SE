---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---


# Orchestrate-dispositionsaktiviteter {#activities}

När du har skapat en komposition kan du börja organisera de olika uppgifter som ska utföras. För att göra detta finns en visuell arbetsyta som du kan använda för att skapa ett kompositionsdiagram. I det här diagrammet kan du lägga till olika aktiviteter och koppla dem i en sekventiell ordning.

## Lägg till aktiviteter {#add}

I det här skedet av konfigurationen visas diagrammet med en startikon som representerar början av arbetsflödet. Om du vill lägga till din första aktivitet klickar du på knappen **+** som är ansluten till startikonen.

En lista över aktiviteter som kan läggas till i diagrammet visas. Vilka aktiviteter som är tillgängliga beror på var du befinner dig i dispositionsdiagrammet. När du till exempel lägger till din första aktivitet kan du starta kompositionen genom att rikta in dig på en målgrupp, dela arbetsflödessökvägen, ange inställningar för att fördröja arbetsflödets körning eller ange en **Vänta** -aktivitet för att fördröja arbetsflödets körning. Efter en **Bygg målgrupp** kan du å andra sidan förfina ditt mål med riktade aktiviteter eller organisera dispositionsprocessen med flödeskontrollaktiviteter.

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

* **Flera markeringar**: Markera flera aktiviteter om du vill ta bort alla samtidigt eller kopiera och klistra in dem. Se [det här avsnittet](#copy).
* **Rotera**: Växla arbetsytan lodrätt.
* **Anpassa till skärmen**: Anpassa arbetsytans zoomnivå till skärmen.
* **Zooma ut** / **Zooma in**: Zooma ut eller in på arbetsytan.
* **Visningsschema**: Öppnar en ögonblicksbild av arbetsytan som visar att du finns.

## Hantera aktiviteter {#manage}

När du lägger till aktiviteter är åtgärdsknappar tillgängliga i egenskapsrutan, vilket gör att du kan utföra flera åtgärder.

![](assets/activity-actions.png)

Du kan:

* **Ta bort** aktiviteten från arbetsytan.
* **Inaktivera/aktivera** aktiviteten. När arbetsflödet körs körs inte inaktiverade aktiviteter och följande aktiviteter på samma sökväg, och arbetsflödet stoppas.
* **Pausa/återuppta** aktiviteten. När arbetsflödet körs pausas det vid den pausade aktiviteten. Motsvarande uppgift och alla som följer den i samma sökväg körs inte.
* **Kopiera** aktiviteten och klistra in den på en annan plats i kompositionen. Det gör du genom att klicka på knappen **+** för en övergång och välja Klistra in X-aktivitet. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Konfigurera **körningsalternativ** för den valda aktiviteten. Expandera avsnittet nedan om du vill veta mer om de tillgängliga alternativen.

  +++Tillgängliga körningsalternativ

  I avsnittet **Egenskaper** kan du konfigurera allmänna inställningar för aktivitetens körning:

   * **Körning**: Definiera den åtgärd som ska utföras när programmet startas.
   * **Maximal körningstid**: Ange en varaktighet som 30 eller 1 tim. Om aktiviteten inte är klar efter att den angivna tiden har gått ut utlöses en varning. Detta påverkar inte arbetsflödets funktioner.
   * **Tidszon**: Välj tidszon för aktiviteten. Med Federated Audience Composition kan du hantera tidsskillnader mellan flera länder i samma instans. Inställningen som används konfigureras när instansen skapas.
   * **Tillhörighet**: Tvinga kompositionsaktiviteten att köras på en viss dator. För att kunna göra detta måste du ange en eller flera tillhörigheter för aktiviteten i fråga.
   * **Beteende**: Definiera proceduren som ska följas om asynkrona uppgifter används.

  I avsnittet **Felhantering** kan du ange vilken åtgärd som ska utföras om aktiviteten stöter på ett fel.

  Med avsnittet **Initieringsskript** kan du initiera variabler eller ändra aktivitetsegenskaper. Klicka på knappen **Redigera kod** och skriv det kodfragment som ska köras. Skriptet anropas när aktiviteten körs.

+++

* Åtkomst till aktivitetens **loggar och uppgifter**.
