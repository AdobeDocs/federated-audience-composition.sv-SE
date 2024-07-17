---
audience: end-user
title: Använd aktiviteten Skapa målgrupp
description: Lär dig använda aktiviteten Skapa målgrupp
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

---


# Bygg målgrupper {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Bygg målgruppsaktivitet"
>abstract="Med aktiviteten **Skapa målgrupp** kan du definiera målgruppen som ska ange kompositionen."

Med aktiviteten **Skapa målgrupp** kan du definiera målgruppen som ska ange kompositionen.

Om du vill definiera målgruppspopulationen kan du:

<!--* Select an existing audience, created as a list in the client console.-->
* Välj en Adobe Experience Platform-målgrupp.
* Bygg en ny målgrupp med frågemodelleraren genom att definiera och kombinera filtervillkor.

Aktiviteten **Skapa målgrupp** kan placeras i början av kompositionen eller efter andra aktiviteter. Alla aktiviteter kan placeras efter **Skapa målgrupp**.

## Konfigurera aktiviteten Skapa målgrupp {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Målgrupp"
>abstract="Välj målgrupp."

Följ de här stegen för att konfigurera aktiviteten **Skapa målgrupp**:

1. Lägg till en **Skapa målgruppsaktivitet**.
1. Definiera en etikett.
1. Ange om du vill skapa en målgrupp eller välja en befintlig.
1. Konfigurera målgruppen genom att följa stegen som beskrivs på flikarna nedan.

>[!BEGINTABS]

>[!TAB Skapa målgrupp]

Så här skapar du en egen målgrupp:

1. Välj **Skapa målgrupp**.
1. Välj **Schema**, även kallat måldimension. Med schemat kan du definiera målgruppen för åtgärden: mottagare, avtalspliktiga mottagare, operatör, prenumeranter osv. Som standard väljs schemat bland mottagarna.
1. Klicka på **Fortsätt**.
1. Använd frågemodelleraren för att definiera frågan. [Lär dig arbeta med frågemodelleraren](../../query/query-modeler-overview.md)

>[!TAB Läs målgrupp]

Så här väljer du en befintlig målgrupp:

1. Välj **Läs målgrupp**.
1. Klicka på **Fortsätt**.
1. Välj målgrupp.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
