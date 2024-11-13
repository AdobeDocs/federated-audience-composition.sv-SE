---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Viktiga principer för skapande av kompositioner {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Kompositionsegenskaper"
>abstract="På den här skärmen väljer du den mall som ska användas för att skapa kompositionen och anger en etikett. Expandera sektionen Ytterligare OPTIONS om du vill konfigurera fler inställningar, till exempel kompositionens interna namn, dess mapp, tidszon och övervakningsgrupp. Vi rekommenderar starkt att du väljer en grupp för ansvariga så att de får ett meddelande om ett fel inträffar."

## Vad innehåller en komposition? {#gs-composition-inside}

Experience Platform Federated Audience Composition har en visuell arbetsyta som gör att du kan skapa målgrupper genom att utnyttja olika aktiviteter (dela, berika osv.).

Kompositionsdiagrammet är en representation av vad som ska hända. Det beskriver de olika åtgärder som ska utföras och hur de är sammankopplade.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Varje komposition innehåller:

* **[!UICONTROL Activities]**: En aktivitet är en uppgift som ska utföras. De olika aktiviteterna visas i diagrammet med ikoner. Varje aktivitet har specifika egenskaper och andra egenskaper som är gemensamma för alla aktiviteter.
* **[!UICONTROL Transitions]**: Övergångar länkar en källaktivitet till en målaktivitet och definierar deras sekvens.
* **[!UICONTROL Worktables]**: Arbetstabellen innehåller all information som följer med övergången. Varje komposition använder flera arbetstabeller. De data som förmedlas i dessa tabeller kan användas under hela kompositionens livscykel.

## Viktiga steg för att skapa en komposition {#gs-composition-steps}

De viktigaste stegen för att skapa en komposition är följande:

1. [Skapa och konfigurera kompositionen](../compositions/create-composition.md)
1. [Organisera aktiviteter](../compositions/orchestrate-activities.md)
1. [Utför kompositionen och övervaka dess körning](../compositions/start-monitor-composition.md)
