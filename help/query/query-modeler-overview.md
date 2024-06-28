---
audience: end-user
title: Arbeta med frågemodelleraren
description: Lär dig arbeta med frågemodelleraren.
source-git-commit: f6730819712ffcbe815517a4406dac7e8fb9779c
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Arbeta med frågemodelleraren {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Frågemodelleraren"
>abstract="Definiera filtreringskriterier för mottagare eller andra måldimensioner från databasen."

Frågemodelleraren förenklar filtreringen av databasen baserat på olika villkor. Dessutom kan frågemodelleraren hantera mycket komplexa och långa frågor effektivt, vilket ger större flexibilitet och precision. Dessutom har den stöd för fördefinierade filter under förhållanden, vilket gör att du enkelt kan förfina dina frågor samtidigt som du använder avancerade uttryck och operatorer för omfattande målgruppsanpassning och segmenteringsstrategier.

## Åtkomst till frågemodelleraren

Frågemodelleraren är tillgänglig i alla sammanhang där du behöver definiera regler för att filtrera data.

| Användning | Exempel |
|  ---  |  ---  |
| **Definiera målgrupper**: Ange den målgrupp du vill rikta in dig på i dina kompositioner och skapa enkelt nya målgrupper som är anpassade efter dina behov. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Anpassa arbetsflödesaktiviteter**: tillämpa regler i arbetsflödesaktiviteter, som **Dela** och **Avstämning**, för att passa in dina specifika krav. [Läs mer om arbetsflödesaktiviteter](../compositions/activities/about-activities.md) | ![](assets/access-workflow.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Fördefinierade filter**: Skapa fördefinierade filter som fungerar som genvägar under olika filtreringsåtgärder, oavsett om du arbetar med datalistor eller skapar en målgrupp för en leverans. | ![](assets/access-predefined-filter.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Anpassa listor**: Skapa anpassade regler för att filtrera data som visas i listor som mottagare, leveranslistor osv. | ![](assets/access-lists.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Gränssnitt för frågemodelleraren {#interface}

Frågemodelleraren innehåller en central arbetsyta där du skapar frågan och en höger ruta med information om frågan.

![](assets/query-interface.png){zoomable="yes"}

### Den centrala arbetsytan {#canvas}

Frågemodellerarens centrala arbetsyta är där du lägger till och kombinerar de olika komponenterna som skapar din fråga. [Lär dig hur du skapar en fråga](build-query.md)

Verktygsfältet i det övre högra hörnet av arbetsytan innehåller alternativ för att enkelt ändra frågekomponenterna och navigera på arbetsytan:

* **Flervalsläge**: Välj flera filterkomponenter som ska kopieras och klistras in på valfri plats.
* **Rotera**: Växla arbetsytan lodrätt.
* **Anpassa till skärm**: Anpassa arbetsytans zoomnivå till skärmen.
* **Zooma ut** / **Zooma in**: Zooma ut eller in på arbetsytan.
* **Visa karta**: Öppnar en ögonblicksbild av arbetsytan som visar att du befinner dig.

### Rutan Regelegenskaper {#rule-properties}

På höger sida, **[!UICONTROL Rule properties]** innehåller information om frågan. Det gör att du kan utföra olika åtgärder för att kontrollera frågan och se till att den passar dina behov. [Lär dig hur du kontrollerar och validerar din fråga](build-query.md#check-and-validate-your-query)
