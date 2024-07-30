---
audience: end-user
title: Kom igång med scheman
description: Lär dig hur du börjar med scheman
badge: label="Begränsad tillgänglighet" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 741f73443471872025f63142e627ca1ed5b428ae
workflow-type: tm+mt
source-wordcount: '423'
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

Genom att skapa ett schema kan du definiera en representation av tabellen i Experience Platform Federated Audience Composition:

* Ge den ett eget namn och en beskrivning som förenklar förståelsen för användaren
* Bestäm synligheten för varje fält utifrån deras verkliga användning
* Välj dess primärnyckel för att länka scheman mellan dem efter behov i [datamodellen](../data-management/gs-models.md#data-model-start)

## Skapa ett schema {#schema-create}

Följ stegen nedan för att skapa scheman i Federated Audience Composition:

1. Gå till länken **[!UICONTROL Models]** i avsnittet **[!UICONTROL FEDERATED DATA]**. Bläddra till fliken **[!UICONTROL Schema]** och klicka på knappen **[!UICONTROL Create schema]**.

   ![](assets/schema_create.png){zoomable="yes"}

   I det här steget får du tillgång till en ny skärm med en listruta där du kan hitta de databaser som är anslutna till din miljö. Läs mer om databasanslutning i [det här avsnittet](../connections/connections.md#connections-fdb).

1. Markera källdatabasen i listan och klicka på fliken **[!UICONTROL Add tables]**.

   ![](assets/schema_tables.png){zoomable="yes"}

   Du kan sedan se en lista över alla tabeller i databasen.

1. Genom att lägga till de tabeller som du vill skapa schemat för får du tillgång till deras fält enligt nedan:

   ![](assets/schema_fields.png){zoomable="yes"}

   För varje tabell kan du:

   * ändra schemats etikett
   * lägg till en beskrivning
   * byta namn på alla fält och ange deras synlighet
   * välj schemats primärnyckel

   För följande importerade tabell:

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   Schemat kan definieras så här:

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## Redigera ett schema {#schema-edit}

Så här redigerar du ett schema:

1. Klicka på schemats namn i schemamappen.

1. Klicka på knappen **[!UICONTROL Edit]**.

   ![](assets/schema_edit.png){zoomable="yes"}

   Du har tillgång till samma alternativ som när du [skapar ett schema](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Förhandsgranska data i ett schema {#schema-preview}

Om du vill förhandsgranska data i tabellen som representeras av ditt schema går du till fliken **[!UICONTROL Data]** enligt nedan.

Klicka på länken **[!UICONTROL Calculate]** om du vill förhandsgranska det totala antalet inspelningar.

![](assets/schema_data.png){zoomable="yes"}

Klicka på knappen **[!UICONTROL Configure columns]** om du vill ändra hur data visas.

![](assets/schema_columns.png){zoomable="yes"}

## Ta bort ett schema {#schema-delete}

Om du vill ta bort ett schema klickar du på knappen **[!UICONTROL More]** och väljer sedan **[!UICONTROL Delete]**.

![](assets/schema_delete.png){zoomable="yes"}
