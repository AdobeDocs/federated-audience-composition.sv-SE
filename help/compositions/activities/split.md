---
audience: end-user
title: Använda aktiviteten Dela
description: Lär dig använda aktiviteten Dela
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Dela {#split}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Delad aktivitet"
>abstract="Med aktiviteten **Dela** kan du segmentera inkommande populationer i flera deluppsättningar baserat på olika urvalskriterier, t.ex. filtreringsregler eller populationsstorlek."

Med aktiviteten **Dela** kan du segmentera inkommande populationer i flera deluppsättningar baserat på olika urvalskriterier, t.ex. filtreringsregler eller populationsstorlek.

## Konfigurera aktiviteten Dela {#split-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segment för delad aktivitet"
>abstract="Lägg till så många delmängder som du vill för att segmentera den inkommande populationen.<br/></br>När aktiviteten **Dela** körs segmenteras populationen mellan de olika delmängderna i den ordning som de läggs till i aktiviteten. Innan du påbörjar kompositionen måste du se till att du har ordnat delmängderna i den ordning som passar dig med pilknapparna."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Dela aktivitetsfilter"
>abstract="Om du vill använda ett filtreringsvillkor för delmängden klickar du på **[!UICONTROL Create filter]** och konfigurerar den önskade filtreringsregeln med frågemodelleraren. Ta till exempel med profiler från den inkommande populationen vars e-postadress finns i databasen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Gräns för delad aktivitet"
>abstract="Om du vill begränsa antalet profiler som markeras av delmängden aktiverar du alternativet **[!UICONTROL Enable limit]** och anger antalet eller procentsatserna för den population som ska inkluderas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Sortering av delad aktivitet"
>abstract="När du anger en populationsgräns för en delmängd kan du rangordna de valda profilerna baserat på ett visst profilattribut i stigande eller fallande ordning. Aktivera alternativet **Aktivera sortering** om du vill göra det. Du kan till exempel begränsa en delmängd så att den endast innehåller de 50 översta profilerna med det högsta inköpspriset."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Delad generering av komplementfärg"
>abstract="När du har konfigurerat alla deluppsättningar kan du välja den återstående populationen som inte matchade någon av deluppsättningarna och inkludera dem i en ytterligare utgående övergång. Aktivera alternativet **Generera komplement** om du vill göra det."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Generera alla delmängder i samma tabell"
>abstract="Växla till det här alternativet om du vill gruppera alla delmängder i en enda utdataövergång."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Hoppa över tom övergång"
>abstract="Aktivera alternativet **[!UICONTROL Skip empty transition]** om du vill inaktivera utdataövergången för den här delmängden om den inkommande populationen är tom."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Aktivera överlappning av utdatapopulationer"
>abstract="Med alternativet **[!UICONTROL Enable overlapping of output populations]** kan du hantera populationer som tillhör flera delmängder. När rutan inte är markerad ser delningsaktiviteten till att en mottagare inte kan finnas i flera utdataövergångar, även om den uppfyller villkoren för flera delmängder. De kommer att vara i målet för den första fliken med matchande villkor. När rutan är markerad kan mottagarna hittas i flera delmängder om de uppfyller filtervillkoren. Adobe Campaign rekommenderar att man använder exklusiva kriterier."

Följ de här stegen för att konfigurera aktiviteten **Dela**:

1. Lägg till en **delad**-aktivitet i kompositionen.

1. Aktivitetskonfigurationsrutan öppnas med en standarddelmängd. Klicka på knappen **Lägg till segment** om du vill lägga till så många delmängder som behövs för att segmentera den inkommande populationen.

   >[!IMPORTANT]
   >
   >När aktiviteten **Dela** körs segmenteras populationen över de olika delmängderna i den ordning som de läggs till i aktiviteten. Om till exempel den första delmängden återställer 70 % av den ursprungliga populationen, kommer nästa tillagda delmängd endast att tillämpa sina urvalskriterier på de återstående 30 %, och så vidare.
   >
   >Innan du påbörjar kompositionen måste du se till att du har beställt delmängderna i den ordning som passar dina behov. Det gör du genom att använda pilknapparna för att ändra positionen för en delmängd.

1. När deluppsättningar har lagts till visar aktiviteten så många utdataövergångar som det finns deluppsättningar. Vi rekommenderar starkt att du ändrar etiketten för varje delmängd så att du enkelt kan identifiera dem på arbetsytan.

   ![](../assets/split.png)

1. Konfigurera hur varje delmängd ska filtrera den inkommande populationen. Följ dessa steg för att göra detta:

   1. Expandera delmängden för att visa dess egenskaper.

      ![](../assets/split-subset.png)

   1. Om du vill använda ett filtreringsvillkor för delmängden klickar du på **[!UICONTROL Create filter]** och konfigurerar den önskade filtreringsregeln med frågemodelleraren. Ta till exempel med profiler från den inkommande populationen vars e-postadress finns i databasen. [Lär dig arbeta med frågemodelleraren](../../query/query-modeler-overview.md)

   1. Om du vill begränsa antalet profiler som markeras av delmängden aktiverar du alternativet **[!UICONTROL Enable limit]** och anger antalet eller procentsatserna för den population som ska inkluderas.

   1. Om du vill inaktivera en övergång om den inkommande populationen är tom aktiverar du alternativet **[!UICONTROL Skip empty transition]**. Om ingen profil matchar delmängden kommer kompositionen inte att övergå till nästa aktivitet.

   >[!NOTE]
   >
   >När du anger en populationsgräns för en delmängd kan du rangordna de valda profilerna baserat på ett visst profilattribut i stigande eller fallande ordning. Aktivera alternativet **[!UICONTROL Enable sorting]** om du vill göra det. Du kan till exempel begränsa en delmängd så att den endast innehåller de 50 översta profilerna med det högsta inköpspriset.

1. När du har konfigurerat alla deluppsättningar kan du välja den återstående populationen som inte matchade någon av deluppsättningarna och inkludera dem i en ytterligare utgående övergång. Aktivera alternativet **[!UICONTROL Generate complement]** om du vill göra det.

   >[!NOTE]
   >
   >Med alternativet **[!UICONTROL Generate all subsets in the same table]** kan du gruppera alla delmängder till en enda utdataövergång.

1. Med alternativet **[!UICONTROL Enable overlapping of output populations]** kan du hantera populationer som tillhör flera delmängder:

   * När rutan inte är markerad ser delningsaktiviteten till att en mottagare inte kan finnas i flera utdataövergångar, även om den uppfyller villkoren för flera delmängder. De kommer att vara i målet för den första fliken med matchande villkor.
   * När rutan är markerad kan mottagarna hittas i flera delmängder om de uppfyller filtervillkoren. Adobe Campaign rekommenderar att man använder exklusiva kriterier.

Aktiviteten är nu konfigurerad. Vid genomförandet segmenteras populationen i de olika delmängderna, i den ordning som de har lagts till i aktiviteten.

<!--
## Example{#split-example}

In the following example, the **[!UICONTROL Split]** activity is used to segment an audience into distinct subsets based on the communication channel that we want to use :

* **Subset 1 "push"**: This subset comprises all profiles who have installed our mobile application.
* **Subset 2 "sms"**: Mobile phone users: For the remaining population that did not fall into Subset 1, subset 2 applies a filtering rule to select profiles with mobile phones in the database.
* **Complement transition**: This transition captures all the remaining profiles that did not match Subset 1 or Subset 2. Specifically, it includes profiles who neither installed the mobile application nor have a mobile phone, such as users who haven't installed the mobile app or lack a registered mobile number.

![](../assets/workflow-split-example.png)
-->
