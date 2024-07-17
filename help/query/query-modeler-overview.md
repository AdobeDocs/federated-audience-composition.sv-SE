---
audience: end-user
title: Arbeta med frågemodelleraren
description: Lär dig arbeta med frågemodelleraren
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Arbeta med frågemodelleraren {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Frågemodelleraren"
>abstract="Definiera filtreringskriterier för mottagare eller andra scheman, som också kallas måldimension, från databasen."

Frågemodelleraren förenklar filtreringen av databasen baserat på olika villkor. Dessutom kan frågemodelleraren hantera mycket komplexa och långa frågor effektivt, vilket ger större flexibilitet och precision. Dessutom har den stöd för fördefinierade filter under förhållanden, vilket gör att du enkelt kan förfina dina frågor samtidigt som du använder avancerade uttryck och operatorer för omfattande målgruppsanpassning och segmenteringsstrategier.

## Åtkomst till frågemodelleraren

Frågemodelleraren är tillgänglig i alla sammanhang där du behöver definiera regler för att filtrera data.

| Användning | Exempel |
|  ---  |  ---  |
| **Definiera målgrupper**: Ange målgruppen i dina kompositioner och skapa enkelt nya målgrupper som är anpassade efter dina behov. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Anpassa aktiviteter**: Använd regler i dispositionsaktiviteter, som **Dela** och **Avstämning**, för att anpassa dem efter dina specifika krav. [Läs mer om dispositionsaktiviteter](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Gränssnitt för frågemodelleraren {#interface}

Frågemodelleraren innehåller en central arbetsyta där du skapar frågan och en höger ruta med information om frågan.

![](assets/query-interface.png){zoomable="yes"}

### Den centrala arbetsytan {#canvas}

Frågemodellerarens centrala arbetsyta är där du lägger till och kombinerar de olika komponenterna som skapar din fråga. [Lär dig skapa en fråga](build-query.md)

Verktygsfältet i det övre högra hörnet av arbetsytan innehåller alternativ för att enkelt ändra frågekomponenterna och navigera på arbetsytan:

* **[!UICONTROL Multiple selection mode]**: Markera flera filterkomponenter som du vill kopiera och klistra in på den plats där du vill ha dem.
* **[!UICONTROL Rotate]**: Växla arbetsytan lodrätt.
* **[!UICONTROL Fit to screen]**: Anpassa arbetsytans zoomnivå till skärmen.
* **[!UICONTROL Zoom out]** / **[!UICONTROL Zoom in]**: Zooma ut eller in på arbetsytan.
* **[!UICONTROL Display map]**: Öppnar en ögonblicksbild av arbetsytan som visar att du finns.

### Rutan Regelegenskaper {#rule-properties}

Till höger visas information om frågan i rutan **[!UICONTROL Rule properties]**. Det gör att du kan utföra olika åtgärder för att kontrollera frågan och se till att den passar dina behov. Den här rutan visas när du skapar en fråga för att skapa en målgrupp. [Lär dig hur du kontrollerar och validerar din fråga](build-query.md#check-and-validate-your-query)
