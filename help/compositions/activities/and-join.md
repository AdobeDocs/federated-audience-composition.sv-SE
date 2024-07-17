---
audience: end-user
title: Använda aktiviteten OCH-join
description: Lär dig hur du använder AND-join-aktiviteten
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join activity"
>abstract="Med aktiviteten **And-join** kan du synkronisera flera körningsgrenar i en komposition. Den aktiveras när alla föregående aktiviteter har slutförts. På så sätt kan du se till att vissa aktiviteter är slutförda innan du fortsätter att köra kompositionen."

Med aktiviteten **AND-join** kan du synkronisera flera körningsgrenar i en komposition.

Den här aktiviteten utlöser endast den utgående övergången när alla inkommande övergångar har aktiverats, det vill säga när alla föregående aktiviteter har slutförts. På så sätt kan du se till att vissa aktiviteter har slutförts innan du fortsätter att köra kompositionen.

## Konfigurera aktiviteten Och-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Konfigurera aktiviteten AND-join"
>abstract="Välj vilka aktiviteter du vill ansluta till. I listrutan **[!UICONTROL Primary set]** väljer du vilken ingående övergångspopulation du vill behålla."

Följ de här stegen för att konfigurera aktiviteten **AND-join**:

1. Lägg till flera aktiviteter för att bilda minst två olika körningsgrenar.
1. Lägg till en **AND-join**-aktivitet i någon av grenarna.

   ![](../assets/and-join.png)

1. I avsnittet **[!UICONTROL Merging options]** markerar du alla tidigare aktiviteter som du vill synkronisera.
1. I listrutan **[!UICONTROL Primary set]** väljer du vilken ingående övergångspopulation du vill behålla. Den utgående övergången kan bara innehålla en av de ingående övergångspopulationerna. Om aktiviteten inte är konfigurerad kommer den utgående övergången att slumpmässigt välja en av de inkommande populationerna.
