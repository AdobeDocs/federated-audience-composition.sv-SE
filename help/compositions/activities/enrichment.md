---
audience: end-user
title: Använd anrikningsaktiviteten
description: Lär dig använda anrikningsaktiviteten
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---


# Berikning {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Anrikningsaktivitet"
>abstract="The **Berikning** kan du förbättra måldata med ytterligare information från databasen. Den används ofta i en komposition efter segmenteringsaktiviteter."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Anrikningsaktivitet"
>abstract="När berikningsdata har lagts till i sammansättningen kan de användas i aktiviteter som lagts till efter **Berikning** -aktivitet för att segmentera profiler i olika grupper baserat på deras beteenden, inställningar och val."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Länkdefinition"
>abstract="Skapa en länk mellan data i arbetstabellen och den federerade databasen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Anrikningsavstämning"
>abstract="Ange avstämningsparametrarna."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Anrikningsdata"
>abstract="Välj de data som ska användas för att berika kompositionen. Du kan välja två typer av anrikningsdata: ett enskilt anrikningsattribut från måldimensionen, eller en samlingslänk, som är en länk med en 1-N-kardinalitet mellan tabellerna."

The **Berikning** kan du förbättra måldata med ytterligare information från den federerade databasen. Den används ofta i kompositioner efter segmenteringsaktiviteter.

Anrikningsdata kan komma antingen:

* **Från samma arbetsregister** som den som är inriktad på din komposition:

  *Ange en grupp kunder som målgrupp och lägg till fältet&quot;Födelsedatum&quot; i den aktuella arbetsregistret*.

* **Från en annan arbetstabell**:

  *Ange kunder som målgrupp och lägg till fälten&quot;Belopp&quot; och&quot;Typ av produkt&quot; från tabellen&quot;Inköp&quot;*.

När anrikningsdata har lagts till i sammansättningen kan de användas i aktiviteter som lagts till efter **Berikning** aktiviteter för att segmentera kunder i olika grupper baserat på deras beteenden, preferenser och val.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Lägg till en anrikningsaktivitet {#enrichment-configuration}

Följ de här stegen för att konfigurera **Berikning** aktivitet:

1. Lägg till aktiviteter som **Bygg målgrupper** och **Kombinera** verksamhet.
1. Lägg till en **Berikning** aktivitet.
1. Om flera övergångar har konfigurerats i din komposition kan du använda **[!UICONTROL Primary set]** -fält för att definiera vilken övergång som ska användas som primär uppsättning för att berika med data.

## Lägg till anrikningsdata {#enrichment-add}

1. Klicka **Lägg till anrikningsdata** och välj det attribut som ska användas för att förbättra data.

   Du kan välja två typer av anrikningsdata: ett enskilt anrikningsattribut från måldimensionen eller en samlingslänk. Var och en av dessa typer beskrivs i exemplen nedan:

   * [Single enrichment-attribut](#single-attribute)
   * [Samlingslänk](#collection-link)

<!--
>[!NOTE]
>
>The **Edit expression button** in the attribute selection screen allows you to build advanced expressions to select the attribute. [Learn how to work with the expression editor](../../query/expression-editor.md)-->

## Skapa länkar mellan tabeller {#create-links}

The **[!UICONTROL Link definition]** kan du skapa en länk mellan data i arbetstabellen och databasen. Om du till exempel läser in data från en fil som innehåller mottagarnas kontonummer, land och e-postadress måste du skapa en länk till landstabellen för att kunna uppdatera informationen i deras profiler.

Det finns flera typer av länkar:

* **[!UICONTROL 1 cardinality simple link]**: Varje post från den primära uppsättningen kan kopplas till en och endast en post från de länkade data.
* **[!UICONTROL 0 or 1 cardinality simple link]**: Varje post i den primära uppsättningen kan kopplas till 0- eller 1-posten från de länkade data, men inte till fler än en.
* **[!UICONTROL N cardinality collection link]**: Varje post från den primära uppsättningen kan kopplas till 0, 1 eller fler (N) poster från länkade data.

Så här skapar du en länk:

1. I **[!UICONTROL Link definition]** klickar du på **[!UICONTROL Add link]** -knappen.

1. I **Relationstyp** väljer du den typ av länk du vill skapa.

1. Identifiera det mål som du vill länka den primära uppsättningen till:

   * Om du vill länka en befintlig tabell i databasen väljer du **[!UICONTROL Database schema]** och välj önskad tabell i **[!UICONTROL Target schema]** fält.
   * Om du vill länka till data från indataövergången väljer du **Tillfälligt schema** och markera den övergång vars data du vill använda.

1. Definiera avstämningskriterierna för att matcha data från den primära uppsättningen med det länkade schemat. Det finns två typer av kopplingar:

   * **Enkelt hörn**: Välj ett specifikt attribut för att matcha data från de två scheman. Klicka **Lägg till join** och väljer **Source** och **Mål** attribut som ska användas som avstämningskriterier.
   * **Avancerad join**: Skapa en koppling med avancerade villkor. Klicka **Lägg till join** och klicka på **Skapa villkor** för att öppna frågemodelleraren.

Ett exempel på komposition med hjälp av länkar finns i [Exempel](#link-example) -avsnitt.

## Exempel {#example}

### Single enrichment-attribut {#single-attribute}

Här lägger vi bara till ett enda anrikningsattribut, till exempel födelsedatumet. Följ de här stegen:

1. Klicka inuti **Attribut** fält.
1. Välj ett enkelt fält från målgruppsdimensionen, födelsedatumet i vårt exempel.
1. Klicka **Bekräfta**.

### Samlingslänk {#collection-link}

I det här mer komplicerade fallet väljer vi en samlingslänk som är en länk med en 1-N-kardinalitet mellan tabellerna. Vi hämtar de tre senaste inköpen som är mindre än 100$. Därför måste du definiera:

* ett anrikningsattribut: **Totalt belopp** fält
* antalet rader som ska hämtas: 3
* ett filter: filtrera bort objekt som är större än 100$
* en sortering: underordnad sortering på **Orderdatum** fält.

#### Lägg till attributet {#add-attribute}

Här väljer du den samlingslänk som ska användas som anrikningsdata.

1. Klicka inuti **Attribut** fält.
1. Klicka **Visa avancerade attribut**.
1. Välj **Totalt belopp** fält från **Inköp** tabell.

#### Definiera samlingsinställningarna{#collection-settings}

Definiera sedan hur data samlas in och hur många poster som ska hämtas.

1. Välj **Samla in data** i **Välj hur data samlas in** nedrullningsbar meny.
1. Skriv&quot;3&quot; i dialogrutan **Rader att hämta (kolumner att skapa)** fält.

Om du t.ex. vill få fram genomsnittligt antal inköp för en kund väljer du **Sammanställda data** i stället, och markera **Genomsnittlig** i **Sammanställningsfunktion** nedrullningsbar meny.

#### Definiera filtren{#collection-filters}

Här definierar vi det högsta värdet för anrikningsattributet. Vi filtrerar bort objekt som är större än 100$. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. Klicka **Redigera filter**.
1. Lägg till följande två filter: **Totalt belopp** finns AND **Totalt belopp** är mindre än 100. Den första filtrerar NULL-värden så som de skulle visas som det största värdet.
1. Klicka **Bekräfta**.

#### Definiera sorteringen{#collection-sorting}

Vi måste nu använda sortering för att hämta de tre **senaste** inköp.

1. Aktivera **Aktivera sortering** alternativ.
1. Klicka inuti **Attribut** fält.
1. Välj **Orderdatum** fält.
1. Klicka **Bekräfta**.
1. Välj **Fallande** från **Sortera** nedrullningsbar meny.


### Berika med länkade data {#link-example}

I exemplet nedan visas en komposition som konfigurerats för att skapa en länk mellan två övergångar. De första övergångarna avser profildata med hjälp av en Query-aktivitet, medan den andra övergången omfattar inköpsdata som lagras i en fil som läses in via en Load file-aktivitet.

* Den första **Berikning** aktivitetslänkar vår primära uppsättning (data från **Fråga** aktivitet) med schemat från **Läs in fil** aktivitet. På så sätt kan vi matcha varje profil som används av frågan med motsvarande inköpsdata.
* En sekund **Berikning** aktiviteten läggs till för att berika data från sammansättningstabellen med inköpsdata från **Läs in fil** aktivitet. Detta gör att vi kan använda dessa data i ytterligare aktiviteter, till exempel för att anpassa meddelanden som skickas till kunderna med information om deras köp.





<!--

Add other fields
use it in delivery


cardinality between the tables (1-N)
1. select attribute to use as enrichment data

    display advanced fields option
    i button

    note: attributes from the target dimension

1. Select how the data is collected
1. number of records to retrieve if want to retrieve a collection of multiple records
1. Apply filters and build rule

    select an existing filter
    save the filter for reuse
    view results of the filter visually or in code view

1. sort records using an attribute

leverage enrichment data in campaign

where we can use the enrichment data: personalize email, other use cases?

## Example

-->
