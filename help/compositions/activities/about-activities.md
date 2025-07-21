---
audience: end-user
title: Arbeta med aktiviteter
description: Lär dig arbeta med aktiviteter
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---

# Arbeta med aktiviteter {#activities}

I Federated Audience Composition kan du skapa kompositioner med två typer av aktiviteter:

* Med **målaktiviteter** kan du skapa ett eller flera mål genom att definiera en målgrupp och dela eller kombinera dessa målgrupper med hjälp av korsnings-, union- eller exkluderingsåtgärder.
* **Flödeskontrollaktiviteter** är specifika för att organisera och köra kompositioner. Deras huvuduppgift är att samordna de andra aktiviteterna.

## Målinriktade aktiviteter

* [Skapa målgruppsaktivitet](build-audience.md): Definiera målpopulationen. Du kan antingen välja en befintlig målgrupp eller använda frågemodelleraren för att definiera en egen fråga.
* [Ändra datakälla](./change-data-source.md): Ändra datakällan som används i kompositionen.
* [Ändra dimension](change-dimension.md): Ändra schemat, även kallat måldimension, när du skapar din komposition.
* [Kombinera](combine.md): Utför segmentering på den inkommande populationen. Du kan använda en union, en skärning eller ett undantag.
* [Deduplicering](deduplication.md): Ta bort dubbletter i resultatet/resultaten av inkommande aktiviteter.
* [Berikning](enrichment.md): Definiera ytterligare data som ska bearbetas i kompositionen. Med den här aktiviteten kan du utnyttja den inkommande övergången och konfigurera aktiviteten för att slutföra utdataövergången med ytterligare data.
* [Avstämning](reconciliation.md): Definiera länken mellan data i databasen och data i en arbetstabell, till exempel data som lästs in från en extern fil.
* [Spara målgrupp](save-audience.md): Uppdatera en befintlig målgrupp eller skapa en ny målgrupp från populationen som beräknas uppströms i en komposition.
* [Dela](split.md): Segmentera inkommande population i flera deluppsättningar.

## Flödeskontrollaktiviteter

* [AND-join](and-join.md): Synkronisera flera körningsgrenar för en komposition.
* **Slut**: Markera slutet av en komposition grafiskt. Denna aktivitet har ingen funktionell inverkan och är därför frivillig.
* [Förgrening](fork.md): Skapa utgående övergångar om du vill starta flera aktiviteter samtidigt.
* [Schemaläggare](scheduler.md): Schemalägg när kompositionen startas.
* [Vänta](wait.md): Pausa körningen av en del av en komposition tillfälligt.
