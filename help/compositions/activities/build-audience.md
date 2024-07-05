---
audience: end-user
title: Använd aktiviteten Skapa målgrupp
description: Lär dig använda aktiviteten Skapa målgrupp
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Bygg målgrupper {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Bygg målgruppsaktivitet"
>abstract="The **Bygg målgrupper** kan du definiera målgruppen som ska delta i kompositionen."

The **Bygg målgrupper** kan du definiera målgruppen som ska delta i kompositionen.

Om du vill definiera målgruppspopulationen kan du:

<!--* Select an existing audience, created as a list in the client console.-->
* Välj en Adobe Experience Platform-målgrupp.
* Bygg en ny målgrupp med frågemodelleraren genom att definiera och kombinera filtervillkor.

The **Bygg målgrupper** kan placeras i början av kompositionen eller efter annan aktivitet. Alla aktiviteter kan placeras efter **Bygg målgrupper**.

## Konfigurera aktiviteten Skapa målgrupp {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Målgrupp"
>abstract="Välj målgrupp."

Följ de här stegen för att konfigurera **Bygg målgrupper** aktivitet:

1. Lägg till en **Bygg målgrupper** aktivitet.
1. Definiera en etikett.
1. Definiera målgruppstyp: **Skapa en egen** eller **Läsa målgrupper**.
1. Konfigurera målgruppen genom att följa stegen som beskrivs på flikarna nedan.

>[!BEGINTABS]

>[!TAB Skapa en egen (fråga)]

Så här skapar du en egen fråga:

1. Välj **Skapa en egen (fråga)**.
1. Välj **Måldimension**. Med målinriktningsdimensionen kan du definiera målgruppen för operationen: mottagare, mottagare, operatör, prenumeranter osv. Som standard är målet markerat bland mottagarna.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Klicka **Fortsätt**.
1. Använd frågemodelleraren för att definiera frågan, på samma sätt som du skapar en målgrupp när du utformar ett nytt e-postmeddelande. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Läs målgrupp]

Så här väljer du en befintlig målgrupp:

1. Välj **Läsa målgrupper**.
1. Klicka **Fortsätt**.
1. Välj målgrupp på samma sätt som du använder en målgrupp när du designar en ny leverans. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
