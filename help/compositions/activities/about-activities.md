---
audience: end-user
title: Arbeta med aktiviteter
description: Lär dig arbeta med aktiviteter
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# Arbeta med aktiviteter {#activities}

I Federated Audience Composition kan du skapa kompositioner med två typer av aktiviteter:

* **Verksamheter som riktar sig till** kan ni skapa ett eller flera mål genom att definiera en målgrupp och dela eller kombinera dessa målgrupper med hjälp av skärnings-, union- eller uteslutningsåtgärder.
* **Flödeskontroll** -aktiviteter är specifika för att organisera och köra kompositioner. Deras huvuduppgift är att samordna de andra aktiviteterna.

## Verksamheter som riktar sig till

* [Bygg målgruppsaktivitet](build-audience.md): Definiera målpopulationen. Du kan antingen välja en befintlig målgrupp eller använda frågemodelleraren för att definiera en egen fråga.
* [Ändra dimension](change-dimension.md): Ändra schemat, även kallat måldimension, när du skapar din komposition.
* [Kombinera](combine.md): Utför segmentering på den inkommande populationen. Du kan använda en union, en skärning eller ett undantag.
* [Deduplicering](deduplication.md): Ta bort dubbletter i resultatet/resultaten av inkommande aktiviteter.
* [Berikning](enrichment.md): Definiera ytterligare data som ska bearbetas i kompositionen. Med den här aktiviteten kan du utnyttja den inkommande övergången och konfigurera aktiviteten för att slutföra utdataövergången med ytterligare data.
* [Avstämning](reconciliation.md): Definiera länken mellan data i databasen och data i en arbetstabell, till exempel data som lästs in från en extern fil.
* [Spara målgrupper](save-audience.md): Uppdatera en befintlig målgrupp eller skapa en ny målgrupp från populationen som beräknas uppströms i en komposition.
* [Dela](split.md): Segmentera inkommande population i flera deluppsättningar.

## Flödeskontroll

* [AND-join](and-join.md): Synkronisera flera körningsgrenar i ett arbetsflöde.
* **End** : Markera slutet av ett arbetsflöde grafiskt. Denna aktivitet har ingen funktionell inverkan och är därför frivillig.
* [Gaffel](fork.md): Skapa utgående övergångar om du vill starta flera aktiviteter samtidigt.
* [Schemaläggare](scheduler.md): Schemalägg när arbetsflödet startas.
* [Vänta](wait.md): Pausa körningen av en del av ett arbetsflöde tillfälligt.
