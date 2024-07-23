---
audience: end-user
title: Kom igång med kompositioner
description: Lär dig hur du börjar med kompositioner
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 03b2fc39c6e0c724363c21418ea50691093d4a10
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Kom igång med kompositioner {#compositions}

## Vad är en komposition? {#what}

Med Adobe Audience Composition kan du skapa kompositioner där du kan använda olika aktiviteter (dela, exkludera...) i en visuell arbetsyta för att skapa målgrupper. När det är klart sparas de resulterande målgrupperna i Adobe Experience Platform tillsammans med befintliga målgrupper och kan utnyttjas till målgrupper som Journey Optimizer. [Lär dig arbeta med målgrupper](../start/audiences.md)

![](assets/composition-example.png)

## Få åtkomst till och hantera kompositioner {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Kompositioner"
>abstract="På den här skärmen kan du komma åt den fullständiga listan med kompositioner, kontrollera deras aktuella status, senaste/nästa körningsdatum och skapa en ny komposition."

Kompositioner är tillgängliga från Adobe Experience Platform-menyn **[!UICONTROL Audiences]** på fliken **[!UICONTROL Federated compositions]**.

Från den här skärmen kan du skapa nya kompositioner och komma åt befintliga. Du kan också duplicera eller ta bort en befintlig komposition genom att klicka på ellipsknappen bredvid dess namn.

![](assets/compositions-list.png)

Om du vill förfina listan och enkelt hitta den komposition du söker efter kan du söka i listan och filtrera kompositioner efter deras status eller senaste bearbetningsdatum.

Du kan också anpassa listan genom att lägga till eller ta bort kolumner. Det gör du genom att klicka på knappen **[!UICONTROL Configure column]**s och lägga till eller ta bort önskade utdatakolumner.

![](assets/compositions-columns.png)

## Kompositionsstatus {#status}

Kompositioner kan ha flera statusvärden:

* **[!UICONTROL Draft]**: Kompositionen har skapats och sparats.
* **[!UICONTROL In progress]**: Kompositionen har körts och körs för närvarande.
* **[!UICONTROL Stopped]**: Kompositionskörningen är klar och har stoppats.
* **[!UICONTROL Paused]**: Kompositionskörningen har pausats.
* **[!UICONTROL Erroneous]**: Kompositionskörningen har påträffat ett fel. Öppna kompositionen och öppna loggarna och aktiviteterna för att identifiera felet och åtgärda det.

Detaljerad information om hur du startar och övervakar en komposition finns i [det här avsnittet](../compositions/start-monitor-composition.md).