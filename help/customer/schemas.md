---
audience: end-user
title: Kom igång med scheman
description: Lär dig hur du börjar med scheman
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 1%

---

# Kom igång med scheman {#schemas}

>[!AVAILABILITY]
>
>Du behöver en av följande behörigheter för att komma åt scheman:
>
>-**Hantera federerat schema**
>-**Visa federerat schema**
>
>Mer information om vilka behörigheter som krävs finns i guiden [Access Federated Audience Composition](/help/start/feature-access.md).

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
>abstract="Du kan filtrera scheman baserat på deras källa. Välj en eller flera Federated databaser om du vill visa deras scheman."

## Vad är ett schema? {#schema-start}

Ett schema är en representation av en tabell i databasen. Det är ett objekt i programmet som definierar hur data kopplas till databastabeller.

Genom att skapa ett schema kan du definiera en representation av tabellen i Experience Platform Federated Audience Composition:

* Ge den ett eget namn och en beskrivning som förenklar förståelsen för användaren
* Bestäm synligheten för varje fält utifrån deras verkliga användning
* Välj dess primärnyckel för att länka scheman mellan dem efter behov i [datamodellen](../data-management/gs-models.md#data-model-start)

>[!CAUTION]
>
>När du ansluter flera sandlådor med samma databas måste du använda separata arbetsscheman.
>

## Skapa ett schema {#schema-create}

Följ stegen nedan för att skapa scheman i Federated Audience Composition:

1. Gå till menyn **[!UICONTROL Models]** i avsnittet **[!UICONTROL Federated Data]**. Bläddra till fliken **[!UICONTROL Schema]** och klicka på **[!UICONTROL Create schema]**.

   ![](assets/schema_create.png){zoomable="yes"}

   I det här steget får du tillgång till en ny skärm med en listruta där du kan hitta de databaser som är anslutna till din miljö. Läs mer om databasanslutning i [det här avsnittet](../connections/connections.md#connections-fdb).

1. Välj källdatabasen i listan och klicka på **[!UICONTROL Next]**.

   ![](assets/schema_tables.png){zoomable="yes"}

   Du kan sedan se en lista över alla tabeller i databasen.

1. Markera de tabeller som du vill skapa schemat för.

1. Varje markerad tabell genererar ett schema med de valda kolumnerna. Konfigurera schemat och dess kolumner efter behov.

   ![](assets/schema_fields.png){zoomable="yes"}

   För varje tabell kan du:

   * ändra schemats etikett
   * lägg till en beskrivning
   * ändra namn på alla fältetiketter och ange deras synlighet
   * välj schemats primärnyckel

   Schemat kan definieras så här:

   ![](assets/schema_example.png)

1. När du är klar med konfigurationen klickar du på **[!UICONTROL Done]**.

## Redigera ett schema {#schema-edit}

Så här redigerar du ett schema:

1. Få åtkomst till det schema du skapat tidigare.

1. Klicka på knappen **[!UICONTROL Edit]**.

   ![](assets/schema_edit.png){zoomable="yes"}

1. I fönstret **[!UICONTROL Edit schema]** kan du komma åt och konfigurera samma alternativ som när du [skapar ett schema](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Förhandsgranska data i ett schema {#schema-preview}

Om du vill förhandsgranska data i tabellen som representeras av ditt schema går du till fliken **[!UICONTROL Data]** enligt nedan.

Klicka på länken **[!UICONTROL Calculate]** om du vill förhandsgranska det totala antalet inspelningar.

![](assets/schema_data.png){zoomable="yes"}

Klicka på knappen **[!UICONTROL Configure columns]** om du vill ändra hur data visas.

![](assets/schema_columns.png){zoomable="yes"}

## Uppdatera ett schema {#schema-refresh}

Tabeller i en federerad databas kan uppdateras, läggas till eller tas bort. I sådana fall måste du uppdatera schemat i Adobe Experience Platform så att det anpassas till de senaste ändringarna. Klicka på de tre punkterna bredvid namnet på schemat som ska uppdateras och välj **Uppdatera schema**.

Du kan också uppdatera schemadefinitionen när du redigerar den.

![](assets/schema_refresh.png){zoomable="yes"}


## Ta bort ett schema {#schema-delete}

Om du vill ta bort ett schema klickar du på knappen **[!UICONTROL More]** och väljer sedan **[!UICONTROL Delete]**.

![](assets/schema_delete.png){zoomable="yes"}
