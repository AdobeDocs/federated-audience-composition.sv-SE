---
audience: end-user
title: Använda aktiviteten OCH-join
description: Lär dig hur du använder AND-join-aktiviteten
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join activity"
>abstract="The **Och-join** kan du synkronisera flera körningsgrenar av en komposition. Den aktiveras när alla föregående aktiviteter har slutförts. På så sätt kan du se till att vissa aktiviteter är slutförda innan du fortsätter att köra kompositionen."

The **Och-join** kan du synkronisera flera körningsgrenar av en komposition.

Den här aktiviteten utlöser endast den utgående övergången när alla inkommande övergångar har aktiverats, det vill säga när alla föregående aktiviteter har slutförts. På så sätt kan du se till att vissa aktiviteter har slutförts innan du fortsätter att köra kompositionen.

## Konfigurera aktiviteten Och-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Konfigurera aktiviteten AND-join"
>abstract="Välj vilka aktiviteter du vill ansluta till. I **Primär uppsättning** väljer du vilken inkommande övergångspopulation som du vill behålla."

Följ de här stegen för att konfigurera **AND-join** aktivitet:

1. Lägg till flera aktiviteter, till exempel kanalaktiviteter, för att bilda minst två olika utförandegrenar.
1. Lägg till en **AND-join** till någon av grenarna.
1. I **Sammanfogningsalternativ** markerar du alla tidigare aktiviteter du vill delta i.
1. I **Primär uppsättning** väljer du vilken inkommande övergångspopulation som du vill behålla. Den utgående övergången kan bara innehålla en av de ingående övergångspopulationerna.

