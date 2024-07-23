---
audience: end-user
title: Kom igång med scheman
description: Lär dig hur du börjar med scheman
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 75d539eef7b36b721c0df52b2fe9115728cf14d3
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

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

Ett schema är en representation av en tabell i databasen. Det är ett objekt i programmet som definierar hur data kopplas till databastabeller.

Genom att skapa ett schema kan du ändra tabellen i FAC:
- Ge den ett eget namn och en beskrivning som förenklar förståelsen för användaren
- Bestäm vilka fält som ska visas utifrån deras verkliga användning
- Välj dess primärnyckel för att länka scheman mellan dem efter behov i [datamodellen](../data-management/gs-models.md#data-model-start)

## Skapa ett schema {#schema-create}

Följ stegen nedan för att skapa scheman i FAC:
Gå till länken **[!UICONTROL Models]** i avsnittet **[!UICONTROL FEDERATED DATA]**. Där finns fliken **[!UICONTROL Schema]**.
Klicka på knappen **[!UICONTROL Create schema]**.

![](assets/schema_create.png){zoomable="yes"}

Du får tillgång till ett nytt gränssnitt med en listruta där du hittar
alla databaser som är anslutna till programmet. Läs mer om [databasanslutning](../connections/connections.md#connections-fdb).
Välj källdatabasen i listan och klicka på fliken **[!UICONTROL Add tables]**

![](assets/schema_tables.png){zoomable="yes"}

Du får tillgång till listan över alla tabeller i databasen.

Genom att lägga till tabellerna, som du vill skapa schemat för, får du tillgång till deras fält enligt nedan.

![](assets/schema_fields.png){zoomable="yes"}

För varje tabell kan du:
- ändra namn på schemaetiketten som angetts
- lägg till en beskrivning
- ändra namn på alla fält och bestämma deras synlighet.
- välj schemats primärnyckel

Här visas en tabell som importerats, precis efter den här typen av tillägg:

![](assets/schema_lumaorder.png){zoomable="yes"}

Schemat kan definieras så här:

![](assets/schema_lumaorders.png){zoomable="yes"}

## Redigera ett schema {#schema-edit}

Om du vill redigera ett schema klickar du på schemats namn i schemamappen. Du har tillgång till sidan nedan.
Klicka på knappen **[!UICONTROL Edit]**.

![](assets/schema_edit.png){zoomable="yes"}

Du har tillgång till samma möjlighet som när du skapar schemat:
- ändra namn på schemaetiketten som angetts
- lägg till en beskrivning
- ändra namn på alla fält och bestämma deras synlighet.
- välj schemats primärnyckel

![](assets/schema_edit_orders.png){zoomable="yes"}

## Förhandsgranska data i ett schema {#schema-preview}

Om du vill förhandsgranska data i tabellen som representeras av ditt schema går du till fliken **[!UICONTROL Data]** enligt nedan.
Du kan få totalt antal inspelningar genom att klicka på länken **[!UICONTROL Calculate]**.

![](assets/schema_data.png){zoomable="yes"}

Du kan ändra översikten över data genom att klicka på knappen **[!UICONTROL Configure columns]**.

![](assets/schema_columns.png){zoomable="yes"}

## Ta bort ett schema {#schema-delete}

Om du vill ta bort ett schema klickar du på knappen **[!UICONTROL More]** och sedan på **[!UICONTROL Delete]**.

![](assets/schema_delete.png){zoomable="yes"}