---
audience: end-user
title: Använd aktiviteten Deduplicering
description: Lär dig hur du använder aktiviteten Deduplicering
source-git-commit: 56d9cc6489557c12761cd3fe8f3b7a61a71ece21
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 19%

---


# Deduplicering {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Fält som identifierar dubbletter"
>abstract="I **Fält som identifierar dubbletter** klickar du på **Lägg till attribut** för att ange de fält där identiska värden gör det möjligt att identifiera dubbletter, t.ex. e-postadress, förnamn, efternamn osv. I fältordningen kan du ange vilka som ska behandlas först."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Dedupliceringsaktivitet"
>abstract="The **Deduplicering** kan du ta bort dubbletter i resultatet av inkommande aktiviteter. Det används främst efter målinriktningsaktiviteter och före aktiviteter som tillåter användning av målinriktade data."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Generera ett komplement"
>abstract="Du kan generera ytterligare en utgående övergång med den återstående populationen, som har uteslutits som en dubblett. Aktivera **Generera komplement** option"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Inställningar för borttagning av dubbletter"
>abstract="Om du vill ta bort dubbletter i inkommande data definierar du dedupliceringsmetoden i fälten nedan. Som standard sparas bara en post. Du bör också välja dedupliceringsläget baserat på ett uttryck eller ett attribut. Som standard väljs den post som ska hållas utanför dubbletterna slumpmässigt."

The **Deduplicering** Med -aktivitet kan du ta bort dubbletter i resultatet av de inkommande aktiviteterna, till exempel duplicerade profiler i mottagarlistan. The **Deduplicering** aktiviteten används vanligtvis efter målinriktade aktiviteter och före aktiviteter som tillåter användning av måldata.

## Konfigurera aktiviteten Deduplicering{#deduplication-configuration}

Följ de här stegen för att konfigurera **Deduplicering** aktivitet:

1. Lägg till en **Deduplicering** till din komposition.

1. Om aktiviteten har flera inkommande övergångar väljer du den övergång som ska användas för att utföra borttagning av dubbletter från **[!UICONTROL Primary set]** listruta

1. I **Fält som identifierar dubbletter** klickar du på **Lägg till attribut** för att ange de fält där identiska värden gör det möjligt att identifiera dubbletter, t.ex. e-postadress, förnamn, efternamn osv. I fältordningen kan du ange vilka som ska behandlas först.

   ![](../assets/deduplication.png)

1. I **Inställningar för borttagning av dubbletter** väljer du antalet unika **Dubbletter att behålla**. Standardvärdet för det här fältet är 1. Med värdet 0 kan du behålla alla dubbletter.

   Om till exempel posterna A och B betraktas som dubbletter av posten Y, och en post C betraktas som en dubblett av posten Z:

   * Om värdet för fältet är 1: endast Y- och Z-posterna behålls.
   * Om värdet för fältet är 0: alla register förs.
   * Om värdet för fältet är 2: Posterna C och Z förvaras och två poster från A, B och Y sparas, av en tillfällighet eller beroende på vilken dedupliceringsmetod som valts därefter.

1. Välj **Dedupliceringsmetod** att använda:

   * **Slumpmässig markering**: Markerar slumpmässigt den post som ska tas bort från dubbletterna.
   * **Använda ett uttryck**: Behåll de poster där det angivna uttryckets värde är det minsta eller det största.
   * **Värden som inte är tomma**: Behåll de poster som uttrycket inte är tomt för.
   * **Följ en lista med värden**: Definiera en värdeprioritet för ett eller flera fält. Definiera värdena genom att klicka **Attribut** om du vill markera ett fält eller skapa ett uttryck och sedan lägga till värdena i rätt tabell. Om du vill definiera ett nytt fält klickar du på **Knappen Lägg till** som finns ovanför listan med värden.

1. Kontrollera **Generera komplement** om du vill utnyttja den återstående populationen. Komplementet består av alla dubbletter. Därefter läggs ytterligare en övergång till aktiviteten.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
