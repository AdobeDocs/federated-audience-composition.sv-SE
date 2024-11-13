---
audience: end-user
title: Använd aktiviteten Deduplicering
description: Lär dig hur du använder aktiviteten Deduplicering
exl-id: 55db2461-fcfb-4284-9ab7-7cb01071ed1c
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 4%

---

# Deduplicering {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Fält som identifierar dubbletter"
>abstract="Klicka på knappen **[!UICONTROL Add attribute]** i avsnittet **[!UICONTROL Fields to identify duplicates]** för att ange de fält där identiska värden gör att dubbletter kan identifieras, till exempel e-postadress, förnamn, efternamn osv. I fältordningen kan du ange vilka som ska behandlas först."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Dedupliceringsaktivitet"
>abstract="Med aktiviteten **Deduplicering** kan du ta bort dubbletter i resultatet av inkommande aktiviteter. Det används främst efter målinriktningsaktiviteter och före aktiviteter som tillåter användning av målinriktade data."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Generera ett komplement"
>abstract="Du kan generera ytterligare en utgående övergång med den återstående populationen, som har uteslutits som en dubblett. Aktivera alternativet **[!UICONTROL Generate complement]** om du vill göra det"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Inställningar för borttagning av dubbletter"
>abstract="Om du vill ta bort dubbletter i inkommande data definierar du dedupliceringsmetoden i fälten nedan. Som standard sparas bara en post. Du bör också välja dedupliceringsläget baserat på ett uttryck eller ett attribut. Som standard väljs den post som ska hållas utanför dubbletterna slumpmässigt."

Med aktiviteten **Deduplicering** kan du ta bort dubbletter i resultatet av de inkommande aktiviteterna, till exempel duplicerade profiler i mottagarlistan. Aktiviteten **Deduplicering** används vanligtvis efter målinriktningsaktiviteter och före aktiviteter som tillåter användning av måldata.

## Konfigurera aktiviteten Deduplicering{#deduplication-configuration}

Så här konfigurerar du aktiviteten **Deduplicering**:

1. Lägg till en **borttagning av dubbletter**-aktivitet i kompositionen.

1. Om aktiviteten har flera inkommande övergångar väljer du den övergång som ska användas för borttagning av dubbletter i listrutan **[!UICONTROL Primary set]**

1. Klicka på knappen **[!UICONTROL Add attribute]** i avsnittet **[!UICONTROL Fields to identify duplicates]** för att ange de fält där identiska värden gör att dubbletter kan identifieras, till exempel e-postadress, förnamn, efternamn osv. I fältordningen kan du ange vilka som ska behandlas först.

   ![](../assets/deduplication.png)

1. I avsnittet **[!UICONTROL Deduplication settings]** väljer du antalet unika **[!UICONTROL Duplicates to keep]**. Standardvärdet för det här fältet är **1**. Med värdet **0** kan du behålla alla dubbletter.

   Om till exempel posterna A och B betraktas som dubbletter av posten Y, och en post C betraktas som en dubblett av posten Z:

   * Om värdet för fältet är **1** behålls bara Y- och Z-posterna.
   * Om värdet för fältet är **0** behålls alla poster.
   * Om värdet för fältet är **2** behålls posterna C och Z och två poster från A, B och Y behålls, av misstag eller beroende på vilken borttagningsmetod som valts därefter.

1. Välj **[!UICONTROL Deduplication method]** som ska användas:

   * **[!UICONTROL Random selection]**: Markerar slumpmässigt den post som ska hållas utanför dubbletterna.
   * **[!UICONTROL Using an expression]**: Behåll de poster där det angivna uttryckets värde är det minsta eller det största.
   * **[!UICONTROL Non-empty values]**: Behåll de poster som uttrycket inte är tomt för.
   * **[!UICONTROL Following a list of values]**: Definiera en värdeprioritet för ett eller flera fält. Om du vill definiera värdena klickar du på **[!UICONTROL Attribute]** för att markera ett fält eller skapa ett uttryck och lägger sedan till värdena i rätt tabell. Om du vill definiera ett nytt fält klickar du på **[!UICONTROL Add button]** som finns ovanför listan med värden.

1. Markera alternativet **[!UICONTROL Generate complement]** om du vill utnyttja den återstående populationen. Komplementet består av alla dubbletter. Därefter läggs ytterligare en övergång till aktiviteten.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
