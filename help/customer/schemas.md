---
audience: end-user
title: Kom igång med scheman
description: Lär dig hur du börjar med scheman
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 883ba223f6c78783fae9f6c9617daa1a7e6635de
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# Kom igång med scheman {#schemas}


>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Markera tabeller"
>abstract="Markera de tabeller som ska läggas till för datamodellen."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Nyckel"
>abstract="Välj en nyckel för datavstämning."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Schemats namn"
>abstract="Ange schemats namn."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Schemabeskrivning"
>abstract="Schemabeskrivningen innehåller kolumner, typer och etiketter. Du kan också kontrollera avstämningsnyckeln för schemat. Om du vill uppdatera schemadefinitionen klickar du på pennikonen."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Välj den källdatabas som ska filtreras"
>abstract="Du kan filtrera scheman baserat på deras källa. Markera en eller flera Federated databaser om du vill visa deras scheman."


## Vad är ett schema? {#schema-start}

Ett schema är ett objekt i programmet som definierar hur data kopplas till databastabeller.
Ett schema refererar till en tabell.

## Skapa ett schema {#schema-create}

Gå till länken **[!UICONTROL Models]** i avsnittet **[!UICONTROL FEDERATED DATA]**. Där finns fliken **[!UICONTROL Schema]**.
Klicka på knappen **[!UICONTROL Create schema]**.

![](assets/schema_create.png){zoomable="yes"}

Välj källdatabasen i listrutan och klicka på fliken **[!UICONTROL Add tables]**

![](assets/schema_tables.png){zoomable="yes"}

Du får tillgång till alla tabeller i databasen och kan skapa ett schema för dem.

Genom att lägga till tabellerna får du tillgång till deras fält och kan behålla det du verkligen behöver.

![](assets/schema_fields.png){zoomable="yes"}

## Redigera ett schema {#schema-edit}

Om du vill redigera ett schema klickar du på schemats namn i schemamappen. Du har tillgång till sidan nedan.
Klicka på knappen **[!UICONTROL Edit]**.

![](assets/schema_edit.png){zoomable="yes"}

## Förhandsgranska data i ett schema {#schema-preview}

Om du vill förhandsgranska data i tabellen som representeras av ditt schema går du till fliken **[!UICONTROL Data]** enligt nedan.

![](assets/schema_data.png){zoomable="yes"}

Du kan ändra översikten över data genom att klicka på knappen **[!UICONTROL Configure columns]**.

![](assets/schema_columns.png){zoomable="yes"}

## Ta bort ett schema {#schema-delete}

Om du vill ta bort ett schema klickar du på knappen **[!UICONTROL More]** och sedan på **[!UICONTROL Delete]**.

![](assets/schema_delete.png){zoomable="yes"}