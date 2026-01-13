---
audience: end-user
title: Kom igång med datamodeller
description: Lär dig hur du börjar med datamodeller
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: a91474bc1f552f5c5f84c028fd60bb7e1b8a4f24
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---


# Översikt över modeller

>[!AVAILABILITY]
>
>För att få tillgång till datamodeller måste du ha någon av följande behörigheter:
>
>-**Hantera federerad datamodell**
>-**Visa federerad datamodell**
>
>Mer information om vilka behörigheter som krävs finns i [åtkomstkontrollguiden](/help/governance-privacy-security/access-control.md).

En datamodell är en uppsättning scheman, målgrupper och länkar mellan dem. Du kan använda modeller för att kombinera databasens data med era målgrupper.

I Federated Audience Composition kan du skapa och hantera datamodeller direkt i arbetsytevyn. Detta inkluderar att lägga till scheman och målgrupper samt att definiera länkarna mellan dem baserat på ditt användningsfall.

Läs mer om [scheman](../data-modelling/schemas.md#schema-start) och [målgrupper](../start/audiences.md).

Du kan till exempel se en representation av en datamodell nedan: tabellerna med namn och länkarna mellan dem.

![](assets/models/datamodel.png){zoomable="yes"}

## Skapa en datamodell {#data-model-create}

Så här skapar du en datamodell:

1. Gå till menyn **[!UICONTROL Federated Data]** i avsnittet **[!UICONTROL Models]** och bläddra till fliken **[!UICONTROL Data model]**.

   Markera knappen **[!UICONTROL Create data model]**.

   ![](assets/models/datamodel_create.png){zoomable="yes"}

2. Definiera namnet på datamodellen och välj knappen **[!UICONTROL Create]**.

3. Välj **[!UICONTROL Add schemas]** från din datamodell för att välja det schema som är associerat med din datamodell.

   ![](assets/models/datamodel_schemas.png){zoomable="yes"}

4. Dessutom kan ni lägga till målgrupper i er datamodell. Välj **[!UICONTROL Add Audiences]** om du vill definiera målgrupperna.

   ![](assets/models/datamodel-audiences.png){zoomable="yes"}

5. Upprätta kopplingar mellan tabeller i datamodellen för att säkerställa korrekta datarelationer. Mer information finns i avsnittet [Skapa länkar](#data-model-links).

6. När du är klar med konfigurationen väljer du **[!UICONTROL Save]** för att tillämpa ändringarna.

## Skapa länkar {#data-model-links}

>[!NOTE]
>
>Om du skapar en länk med flera kopplingar kan du bara använda samma kombination av käll- och målscheman en gång.

>[!BEGINTABS]

>[!TAB Tabellvy]

Så här skapar du länkar mellan tabeller i din datamodell på fliken Tabellvy:

1. Markera ikonen ![ med tre punkter ](/help/assets/icons/more.png) följt av **[!UICONTROL Create link]** bredvid en av tabellen, eller välj **[!UICONTROL Create links]** i avsnittet **[!UICONTROL Links]**:

   ![](assets/models/datamodel_createlinks.png){zoomable="yes"}

2. Fyll i det angivna formuläret för att definiera länken.

   ![](assets/models/datamodel_link.png){zoomable="yes"}

   **Kardinalitet**

   * **1-N**: En förekomst av källtabellen kan ha flera motsvarande förekomster av måltabellen, men en förekomst av måltabellen kan ha högst en motsvarande förekomst av källtabellen.

   * **N-1**: en förekomst av måltabellen kan ha flera motsvarande förekomster av källtabellen, men en förekomst av källtabellen kan ha högst en motsvarande förekomst av måltabellen.

   * **1-1**: En förekomst av källtabellen kan ha högst en motsvarande förekomst av måltabellen.

   Om du vill skapa en länk för flera sammanfogningar väljer du plusikonen . Nu kan du skapa flera kopplingar mellan schemafälten.

   ![Plustecknet är markerat, vilket gör att du kan skapa flera sammanfogningslänkar för modellen.](assets/models/multi-join.png){zoomable="yes"}

Alla länkar som är definierade för din datamodell listas nedan:

![](assets/models/datamodel_alllinks.png){zoomable="yes"}

>[!TAB Arbetsytans vy]

Så här skapar du länkar mellan tabeller i din datamodell på fliken Arbetsytans vy:

1. Öppna arbetsytans vy över din datamodell och välj de två tabeller som du vill länka

2. Markera ![](assets/models/do-not-localize/Smock_AddCircle_18_N.svg)-knappen bredvid Source Join och dra sedan pilen mot Target Join för att upprätta anslutningen.

   ![](assets/models/datamodel.gif){zoomable="yes"}

3. Fyll i det angivna formuläret för att definiera länken och välj **[!UICONTROL Apply]** när den har konfigurerats.

   ![](assets/models/datamodel-canvas-1.png){zoomable="yes"}

   **Kardinalitet**

   * **1-N**: En förekomst av källtabellen kan ha flera motsvarande förekomster av måltabellen, men en förekomst av måltabellen kan ha högst en motsvarande förekomst av källtabellen.

   * **N-1**: en förekomst av måltabellen kan ha flera motsvarande förekomster av källtabellen, men en förekomst av källtabellen kan ha högst en motsvarande förekomst av måltabellen.

   * **1-1**: En förekomst av källtabellen kan ha högst en motsvarande förekomst av måltabellen.

4. Alla länkar som definieras i datamodellen representeras som pilar i arbetsytevyn. Markera en pil mellan två tabeller om du vill visa detaljer, redigera eller ta bort länken efter behov.

   ![](assets/models/datamodel-canvas-2.png){zoomable="yes"}

5. Använd verktygsfältet för att anpassa och justera arbetsytan.

   ![](assets/models/datamodel-canvas-3.png)

   * **[!UICONTROL Zoom in]**: Förstora arbetsytan om du vill visa detaljer om datamodellen tydligare.
   * **[!UICONTROL Zoom out]**: Minska arbetsytans storlek för en bredare vy av datamodellen.
   * **[!UICONTROL Fit view]**: Justera zoomningen så att den passar alla scheman och/eller målgrupper inom det synliga området.
   * **[!UICONTROL Toggle interactivity]**: Aktivera eller inaktivera användarinteraktion med arbetsytan.
   * **[!UICONTROL Filter]**: Välj vilket schema som ska visas på arbetsytan.
   * **[!UICONTROL Force auto layout]**: Ordna scheman och/eller målgrupper automatiskt för bättre organisation.

>[!ENDTABS]

## Videoinstruktioner {#data-model-video}

Lär dig hur du skapar en datamodell i den här videon:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
