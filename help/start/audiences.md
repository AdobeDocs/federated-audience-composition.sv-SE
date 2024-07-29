---
audience: end-user
title: Arbeta med målgrupper
description: Lär dig hur du arbetar med målgrupper
badge: label="Begränsad tillgänglighet" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Arbeta med målgrupper {#gs-audiences}

Med Experience Platform Federated Audience Composition kan du [skapa kompositioner](../compositions/gs-compositions.md), där du kan använda olika aktiviteter i en visuell arbetsyta för att skapa målgrupper och lagra dem i Adobe Experience Platform Audience Portal.

Sedan kan ni rikta in er på de här målgrupperna i Journey Optimizer eller aktivera dem på en målplats som stöds av Adobe Experience Platform.

## Skapa målgrupper med hjälp av kompositioner {#creation}

Om du vill skapa målgrupper med Federated Audience-komposition måste du skapa en komposition med en **[!UICONTROL Save audience]**-aktivitet. Med den här aktiviteten kan du spara målgruppen i Audience Portal och välja fält från externa databaser att inkludera i målgruppen. [Lär dig hur du konfigurerar en Spara målgruppsaktivitet](../compositions/activities/save-audience.md)

Målgrupp som skapats med Adobe Federated Data Composition innehåller alla fält som markerats i aktiviteten **[!UICONTROL Save audience]** och lagras i Audience Portal tillsammans med alla Adobe Experience Platform-målgrupper.

När kompositionen är klar sparas målgruppen i Adobe Experience Platform som en extern målgrupp och finns tillgänglig i Adobe Real-Time Customer Data Platform och/eller Adobe Journey Optimizer.

Du kan aktivera dessa målgrupper till alla målgrupper som stöds av Adobe Experience Platform. Lär dig arbeta med mål i [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}

>[!NOTE]
>
>Publiker som har skapats med Adobe Federated Audience Composition kan inte redigeras. Om du vill göra ändringar i en av dessa målgrupper måste du skapa en ny målgrupp med hjälp av en komposition.

## Nå ut till er målgrupp i Adobe Experience Platform {#access-audience}

Publiker som har skapats med Federated Audience Composition är tillgängliga i Audience Portal, som du kommer åt på menyn **Publiker** .

Fliken **[!UICONTROL Browse]** visar alla befintliga målgrupper som lagras i Adobe Experience Platform. Du kan identifiera personer med Federated Audience Composition i listan med kolumnen **[!UICONTROL Origin]** eller med de filter som finns i den vänstra rutan.

![](assets/audiences-list.png)

Mer information om hur du arbetar med målgrupper i Adobe Experience Platform finns i [dokumentationen för målportalen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->