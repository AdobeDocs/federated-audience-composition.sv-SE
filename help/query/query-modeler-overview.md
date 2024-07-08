---
audience: end-user
title: Arbeta med frågemodelleraren
description: Lär dig hur du arbetar med frågemodelleraren.
source-git-commit: 5d4bdbbb9c903e839b21d22455d870396ac1df7d
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Arbeta med frågemodelleraren {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Fråga modellerare"
>abstract="Definiera filtreringskriterier för mottagare eller något annat schema, även kallat måldimension, från databasen."

Frågemodelleraren förenklar processen med att filtrera databasen baserat på olika kriterier. Dessutom kan frågemodelleraren hantera mycket komplexa och långa frågor effektivt, vilket ger ökad flexibilitet och precision. Dessutom stöder den fördefinierade filter inom villkor, vilket ger dig möjlighet att enkelt förfina dina frågor samtidigt som du använder avancerade uttryck och operatorer för omfattande målgruppsinriktning och segmenteringsstrategier.

## Åtkomst till frågemodelleraren

Frågemodelleraren är tillgänglig i alla sammanhang där du behöver definiera regler för att filtrera data.

| Användning | Exempel |
|  ---  |  ---  |
| **Definiera målgrupper: Ange vilken målgrupp du vill rikta dig till i dina kompositioner och skapa enkelt nya målgrupper** som är skräddarsydda efter dina behov. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Anpassa arbetsflödesaktiviteter**: tillämpa regler inom kompositionsaktiviteter, till exempel **Split** och **Reconciliation**, för att anpassa dig till dina specifika krav. [Läs mer om kompositionsaktiviteter](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Gränssnitt för frågemodellerare {#interface}

Frågemodelleraren tillhandahåller en central arbetsyta där du skapar din fråga och en höger ruta som ger information om din fråga.

![](assets/query-interface.png){zoomable="yes"}

### Den centrala duken {#canvas}

Den centrala arbetsytan för frågemodelleraren är den plats där du lägger till och kombinerar de olika komponenterna som skapar din fråga. [Lär dig hur du skapar en fråga](build-query.md)

Verktygsfältet i det övre högra hörnet på arbetsytan innehåller alternativ för att enkelt ändra frågekomponenterna och navigera på arbetsytan:

* **Flervalsläge**: Välj flera filtreringskomponenter för att kopiera och klistra in dem på valfri plats.
* **Rotera: Växla** arbetsytan vertikalt.
* **Anpassa till skärm**: Anpassa arbetsytans zoomnivå till din skärm.
* **Zooma ut** / **Zooma in**: Zooma ut eller på arbetsytan.
* **Visa karta**: Öppnar en ögonblicksbild av arbetsytan som visar att du befinner dig.

### Fönstret Regelegenskaper {#rule-properties}

Till höger innehåller fönstret **[!UICONTROL Rule properties]** information om din fråga. Det låter dig utföra olika operationer för att kontrollera frågan och se till att den passar dina behov. [Lär dig hur du kontrollerar och validerar din fråga](build-query.md#check-and-validate-your-query)
