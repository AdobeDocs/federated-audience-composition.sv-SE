---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
source-git-commit: fd92c280094989cb64ff5151fb00b4a8b0e650f7
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---


# Orchestrate-dispositionsaktiviteter {#activities}

När du har skapat en komposition kan du börja organisera de olika uppgifter som ska utföras. För att göra detta finns en visuell arbetsyta som du kan använda för att skapa ett kompositionsdiagram. I det här diagrammet kan du lägga till olika aktiviteter och koppla dem i en sekventiell ordning.

## Lägg till aktiviteter {#add}

I det här skedet av konfigurationen visas diagrammet med en startikon som representerar början av arbetsflödet. Om du vill lägga till din första aktivitet klickar du på **+** som är ansluten till startikonen.

En lista över aktiviteter som kan läggas till i diagrammet visas. Vilka aktiviteter som är tillgängliga beror på var du befinner dig i dispositionsdiagrammet. När du till exempel lägger till din första aktivitet kan du starta din komposition genom att rikta in dig på en målgrupp, dela arbetsflödesbanan eller ställa in en **Vänta** för att fördröja arbetsflödets körning. Å andra sidan, efter **Bygg målgrupper** kan du finjustera ditt mål med målinriktade aktiviteter, skicka en leverans till din publik med kanalaktiviteter eller ordna dispositionsprocessen med flödeskontrollaktiviteter.

När en aktivitet har lagts till i diagrammet visas en höger ruta där du kan konfigurera den nyligen tillagda aktiviteten med specifika inställningar. Detaljerad information om hur du konfigurerar varje aktivitet finns i [det här avsnittet](activities/about-activities.md).

Upprepa den här processen om du vill lägga till så många aktiviteter som du vill, beroende på vilka uppgifter du vill att kompositionen ska utföra. Observera att du även kan infoga en ny aktivitet mellan två aktiviteter. Klicka på **+** om övergången mellan aktiviteterna markerar du önskad aktivitet och konfigurerar den i den högra rutan.

Om du vill ta bort en aktivitet markerar du den på arbetsytan och klickar på knappen **Ta bort** -ikonen i aktivitetsegenskaperna.

>[!TIP]
>
>Du kan anpassa namnet på övergångarna mellan varje aktivitet. Det gör du genom att markera övergången och ändra dess etikett i den högra rutan.

## Verktygsfältet {#toolbar}

Verktygsfältet i det övre högra hörnet av arbetsytan innehåller alternativ för att enkelt ändra aktiviteterna och navigera på arbetsytan:

* **Flervalsläge**: Markera flera aktiviteter om du vill ta bort alla samtidigt eller kopiera och klistra in dem. Se [det här avsnittet](#copy).
* **Rotera**: Växla arbetsytan lodrätt.
* **Anpassa till skärm**: Anpassa arbetsytans zoomnivå till skärmen.
* **Zooma ut** / **Zooma in**: Zooma ut eller in på arbetsytan.
* **Visa karta**: Öppnar en ögonblicksbild av arbetsytan som visar att du befinner dig.


## Hantera aktiviteter {#manage}

När du lägger till aktiviteter är åtgärdsknappar tillgängliga i egenskapsrutan, vilket gör att du kan utföra flera åtgärder. Du kan:

* **Ta bort** aktiviteten från arbetsytan.
* **Inaktivera/aktivera** aktiviteten. När arbetsflödet körs körs inte inaktiverade aktiviteter och följande aktiviteter på samma sökväg, och arbetsflödet stoppas.
* **Kopiera** aktiviteten. Se [det här avsnittet](#copy).
* Åtkomst till aktivitetens **Loggar och uppgifter**.
* **Pausa/återuppta** aktiviteten. När arbetsflödet körs pausas det vid den pausade aktiviteten. Motsvarande uppgift och alla som följer den i samma sökväg körs inte.

Flera **Målinriktning** aktiviteter, som **Kombinera** eller **Deduplicering** kan du bearbeta den återstående populationen och inkludera den i en ytterligare utgående övergång. Om du till exempel använder en **Dela** Komplementet består av den population som inte matchar någon av de tidigare definierade delmängderna. Om du vill använda den här funktionen aktiverar du **Generera komplement** alternativ.

## Kopiera aktiviteter {#copy}

Du kan kopiera arbetsflödesaktiviteter och klistra in dem i valfritt arbetsflöde. Målarbetsflödet kan finnas på en annan webbläsarflik.

Du kan kopiera aktiviteter på två sätt:

* kopiera en aktivitet med åtgärdsknappen.

* kopiera flera aktiviteter med verktygsfältsknappen.

Klistra in kopierade aktiviteter genom att klicka på **+** och väljer Klistra in X-aktivitet.

## Körningsalternativ {#execution}

Med alla aktiviteter kan du hantera deras körningsalternativ. Välj en aktivitet och klicka på **Körningsalternativ** -knappen. På så sätt kan du definiera aktivitetens körningsläge och beteende vid fel.

### Egenskaper

The **Körning** I kan du definiera vilken åtgärd som ska utföras när aktiviteten startas.

The **Maximal körningstid** I kan du ange en varaktighet som &quot;30s&quot; eller &quot;1h&quot;. Om aktiviteten inte är klar efter att den angivna tiden har gått ut utlöses en varning. Detta påverkar inte arbetsflödets funktioner.

The **Tidszon** kan du välja aktivitetens tidszon. Med Adobe Campaign kan du hantera tidsskillnader mellan flera länder i samma instans. Inställningen som används konfigureras när instansen skapas.

**Tillhörigheten** kan du tvinga ett arbetsflöde eller en arbetsflödesaktivitet att köras på en viss dator. För att kunna göra detta måste du ange en eller flera tillhörigheter för arbetsflödet eller aktiviteten i fråga.

The **Beteende** I kan du definiera proceduren som ska följas om asynkrona uppgifter används.

### Felhantering

The **Om fel uppstår** kan du ange vilken åtgärd som ska utföras om aktiviteten stöter på ett fel.

### Initieringsskript

The **Initieringsskript** I kan du initiera variabler eller ändra aktivitetsegenskaper. Klicka på **Redigera kod** och skriv det kodfragment som ska köras. Skriptet anropas när aktiviteten körs.

## Exempel {#example}

Här följer ett exempel på ett arbetsflöde som utformats för att skicka ett e-postmeddelande till alla kunder (utom VIP kunder) med ett e-postmeddelande som är intresserade av kaffemaskiner.

För att uppnå detta har följande aktiviteter lagts till:

* A **[!UICONTROL Fork]** Aktivitet som delar upp arbetsflödet i tre banor (en för varje kundgrupp).
* **[!UICONTROL Build audience]** Verksamheter för att inrikta sig på de tre olika kundgrupperna:

   * Kunder med e-post
   * Kunder som tillhör den befintliga målgruppen&quot;Interasted in Coffee Machine(s)&quot;,
   * Kunder som tillhör den befintliga målgruppen&quot;VIP eller belöning&quot;.

* A **[!UICONTROL Combine]** aktiviteter som grupperar kunder med e-post och de som är intresserade av kaffemaskiner,
* A **[!UICONTROL Combine]** verksamhet som utesluter VIP kunder,
* An **[!UICONTROL Email delivery]** aktivitet som skickar ett e-postmeddelande till de resulterande kunderna.

När du är klar med arbetsflödet lägger du till en **[!UICONTROL End]** aktiviteten i slutet av diagrammet. Med den här aktiviteten kan du markera slutet av ett arbetsflöde visuellt och inte ha någon funktionell inverkan.

När du har utformat arbetsflödesdiagrammet kan du köra arbetsflödet och spåra förloppet för dess olika uppgifter.