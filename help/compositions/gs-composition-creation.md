---
audience: end-user
title: Skapa kompositioner
description: Lär dig hur du skapar kompositioner
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Viktiga principer för skapande av kompositioner {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Kompositionsegenskaper"
>abstract="På den här skärmen väljer du den mall som ska användas för att skapa kompositionen och anger en etikett. Expandera sektionen Ytterligare OPTIONS om du vill konfigurera fler inställningar, till exempel kompositionens interna namn, dess mapp, tidszon och övervakningsgrupp. Vi rekommenderar starkt att du väljer en grupp för ansvariga så att de får ett meddelande om ett fel inträffar."

Med Federated Data Composition får du en visuell arbetsyta som gör att du kan skapa målgrupper genom att utnyttja olika aktiviteter (dela, berika osv.).

## Vad finns i en komposition? {#gs-composition-inside}

Kompositionsdiagrammet är en representation av vad som ska hända. Det beskriver de olika åtgärder som ska utföras och hur de är sammankopplade.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Varje komposition innehåller:

* **Verksamhet**: En aktivitet är en uppgift som ska utföras. De olika aktiviteterna visas i diagrammet med ikoner. Varje aktivitet har specifika egenskaper och andra egenskaper som är gemensamma för alla aktiviteter.

  I ett kompositionsdiagram kan en viss aktivitet producera flera uppgifter, särskilt när det finns en slinga eller återkommande åtgärder.

* **Övergångar**: Övergångar länkar en källaktivitet till en målaktivitet och definierar deras sekvens.

* **Worktables**: Arbetstabellen innehåller all information som övergången innehåller. Varje komposition använder flera arbetstabeller. De data som förmedlas i dessa tabeller kan användas under hela kompositionens livscykel.

## Viktiga steg för att skapa en komposition {#gs-composition-steps}

De viktigaste stegen för att skapa en komposition är följande:

1. [Skapa kompositionen](#create)
1. [Konfigurera kompositionens inställningar](#starting-audience)
1. [Lägga till och konfigurera aktiviteter](#action-activities)
1. [Utför kompositionen och övervaka dess körning](#save)
