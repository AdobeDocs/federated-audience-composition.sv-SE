---
audience: end-user
title: Ändra Source-dataaktivitet
description: Lär dig hur du kan använda aktiviteten Ändra datakälla för att ändra datakällan som används i kompositionen, vilket ger större flexibilitet när det gäller att hantera data i en komposition.
exl-id: 8f8e627a-fef9-42b8-a42a-bfa1c421b202
source-git-commit: 59983bb7fd0f8886cc38bfcfc8d7005db4747ac0
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# Ändra datakälla

>[!IMPORTANT]
>
>**[!UICONTROL Change dimension]**- och **[!UICONTROL Change data source]**-aktiviteterna ska **inte** läggas till på en rad. Om du behöver använda båda aktiviteterna i följd inkluderar du en **[!UICONTROL Enrichment]**-aktivitet mellan dem. Detta garanterar att programmet körs på rätt sätt och förhindrar eventuella konflikter och fel.

Med aktiviteten **[!UICONTROL Change data source]** kan du ändra datakällan som används i kompositionen.

## Konfigurera {#configure}

När du har lagt till en **[!UICONTROL Change data source]**-aktivitet på arbetsytan kan du definiera arbetsflödets datakälla.

![Alternativet för datakälla är markerat på arbetsytan för sammanställning av externa målgrupper.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}

| Source | Beskrivning |
| ------ | ----------- |
| Externt FDA-konto | En extern molndatabas som är ansluten till Federated Audience Composition. |

När du har valt **[!UICONTROL FDA external account]** kan du välja vilket externt konto du vill ansluta till.

![Den som visar alternativ för det externa kontot visas.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}
