---
audience: end-user
title: Kom igång med datamodeller
description: Lär dig hur du börjar med datamodeller
badge: label="Begränsad tillgänglighet" type="Informative"
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Kom igång med datamodeller {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="Arbeta med modeller"
>abstract="Scheman och datamodeller visas på den här skärmen. Du kan skapa scheman och datamodeller med knappen **Skapa** ."

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="Välj scheman"
>abstract="Välj scheman för datamodellen."


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="Välj en målgrupp"
>abstract="Välj målgrupp för datamodellen."

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="Datamodellegenskaper"
>abstract="Ange etiketten för datamodellen."


## Vad är en datamodell {#data-model-start}

En datamodell är en uppsättning scheman, målgrupper och länkar mellan dem. Det används för att federera målgrupper med databasdata.

Läs mer om [scheman](../customer/schemas.md#schema-start).

Läs mer om [målgrupper](../start/audiences.md).

Du kan till exempel se en representation av en datamodell nedan: tabellerna med namn och länkar mellan dem.

![](assets/datamodel.png){zoomable="yes"}

I Federated Audience Composition kan du skapa många datamodeller.

De skapas utifrån användningsfallet: du väljer de tabeller som behövs och du länkar dem efter behov.

## Skapa en datamodell {#data-model-create}

Så här skapar du en datamodell:

1. Gå till länken **[!UICONTROL Models]** i avsnittet **[!UICONTROL FEDERATED DATA]** och bläddra till fliken **[!UICONTROL Data model]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Klicka på knappen **[!UICONTROL Create data model]**, definiera namnet på datamodellen och klicka på knappen **[!UICONTROL Create]**.

   ![](assets/datamodel_name.png){zoomable="yes"}

1. Lägg sedan till scheman, målgrupperna och länkarna till datamodellen.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

### Skapa länkar {#data-model-links}

Så här skapar du länkar mellan tabeller i datamodellen:

1. Klicka på **[!UICONTROL Create link]**-menyn i en av tabellerna eller klicka på knappen **[!UICONTROL Create links]** och välj de två tabellerna:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Fyll i det angivna formuläret för att definiera länken.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Kardinalitet**

   * 1-N: en förekomst av källtabellen kan ha flera motsvarande förekomster av måltabellen, men en förekomst av måltabellen kan ha högst en motsvarande förekomst av källtabellen.

   * N-1: en förekomst av måltabellen kan ha flera motsvarande förekomster av källtabellen, men en förekomst av källtabellen kan ha högst en motsvarande förekomst av måltabellen.

   * 1-1: en förekomst av källtabellen kan ha högst en motsvarande förekomst av måltabellen.

Alla länkar som är definierade för datamodellen visas nedan:

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Videoinstruktioner {#data-model-video}

Lär dig hur du skapar en datamodell i den här videon:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
