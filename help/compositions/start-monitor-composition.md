---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
source-git-commit: b946f8821d965fb00f79f6f5557adcfff1ee2387
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---


# Starta och övervaka kompositionen {#start-monitor}

När du har skapat kompositionen och utformat de uppgifter som ska utföras på arbetsytan kan du starta den och övervaka hur den körs.

## Starta kompositionen {#start}

Börja kompositionen genom att navigera till **[!UICONTROL Compositions]** -menyn eller den associerade kampanjen och klicka på **[!UICONTROL Start]** i det övre högra hörnet av arbetsytan.

När kompositionen är klar utförs varje aktivitet på arbetsytan i sekventiell ordning tills kompositionen är klar.

Du kan spåra förloppet för målprofiler i realtid med ett visuellt flöde. På så sätt kan du snabbt identifiera status för varje aktivitet och antalet profiler som övergår mellan dem.

## Dispositionsövergångar {#transitions}

I kompositioner lagras data som överförs från en aktivitet till en annan genom övergångar i ett tillfälligt arbetsregister. Dessa data kan visas för varje övergång. Det gör du genom att markera en övergång och öppna dess egenskaper till höger på skärmen.

* Klicka **[!UICONTROL Preview schema]** för att visa arbetstabellens schema.
* Klicka **[!UICONTROL Preview results]** för att visualisera de data som transporteras i den valda övergången.

## Körning av övervakningsaktivitet {#activities}

Med visuella indikatorer i det övre högra hörnet av varje aktivitetsruta kan du kontrollera deras körning:

| Visuell indikator | Beskrivning |
|-----|------------|
|  | Aktiviteten körs för närvarande. |
|  | Aktiviteten kräver din uppmärksamhet. Detta kan inbegripa att bekräfta leveransen eller vidta nödvändiga åtgärder. |
|  | Aktiviteten har påträffat ett fel. Lös problemet genom att öppna dispositionsloggarna för mer information. |
|  | Aktiviteten har körts. |

## Övervaka loggar och uppgifter {#logs-tasks}

Att övervaka kompositionsloggar och -uppgifter är ett viktigt steg för att analysera kompositionerna och se till att de körs som de ska. De är tillgängliga via **[!UICONTROL Logs]** ikon som är tillgänglig i åtgärdsverktygsfältet och i varje aktivitets egenskapspanel.

The **[!UICONTROL Logs and tasks]** -menyn innehåller en historik över dispositionskörningen, där alla användaråtgärder och påträffade fel registreras. Den här historiken sparas under den tid som anges i kompositionen [körningsalternativ](composition-settings.md). Under den här perioden sparas alla meddelanden, även efter att kompositionen har startats om. Om du inte vill spara meddelandena från en tidigare körning klickar du på **[!UICONTROL Purge history]** -knappen.

Det finns två typer av information:

* The **[!UICONTROL Log]** -fliken innehåller körningshistoriken för alla dispositionsaktiviteter. Den indexerar de åtgärder som utförts och körningsfel i kronologisk ordning.
* The **[!UICONTROL Tasks]** -fliken innehåller information om aktiviteternas körningssekvens.

På båda flikarna kan du välja vilka kolumner som ska visas och i vilken ordning de ska visas, tillämpa filter och använda sökfältet för att snabbt hitta önskad information.

## Kommandon för kompositionskörning {#execution-commands}

Åtgärdsfältet i det övre högra hörnet innehåller kommandon som gör att du kan hantera kompositionskörningen. Du kan:

* **[!UICONTROL Start]** / **[!UICONTROL Resume]** utförandet av kompositionen, som sedan får statusen Pågår. Om kompositionen pausades återupptas den, annars startas den och de inledande aktiviteterna aktiveras sedan.

* **[!UICONTROL Pause]** utförandet av kompositionen, som sedan får statusen Pausad. Inga nya aktiviteter kommer att aktiveras förrän de återupptas, men pågående åtgärder avbryts inte.

* **[!UICONTROL Stop]** en komposition som körs, som sedan får statusen Slutförd. De pågående åtgärderna avbryts om möjligt. Du kan inte återuppta från kompositionen från samma plats som den stoppades.
