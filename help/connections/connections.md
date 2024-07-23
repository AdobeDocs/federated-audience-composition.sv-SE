---
audience: end-user
title: Skapa och hantera anslutningar med federerade databaser
description: Lär dig skapa och hantera anslutningar med Federated Databases
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 5%

---

# Skapa anslutningar {#connections-fdb}

Om du arbetar med en Federated-databas direkt i AEP måste du skapa en anslutning till den.

Om du vill konfigurera en anslutning till databasen går du till avsnittet **[!UICONTROL FEDERATED DATA]** och klickar på knappen **[!UICONTROL Add federated database]** i länken **[!UICONTROL Federated Databases]**.

![](assets/connections_list.png){zoomable="yes"}

Du kommer att få åtkomst till fönstret för anslutningen **[!UICONTROL Properties]**, med namnet och typen av databas.

![](assets/connections_name.png){zoomable="yes"}

Om du väljer dess typ får du tillgång till andra egenskaper som du kan fylla i. [Läs mer här om de databaser som stöds](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

Lär dig mer i länkarna nedan vilken information du behöver för att upprätta anslutningen beroende på vilken typ av databas du använder:

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google Big Query](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Klicka på knappen **[!UICONTROL Test connection]** och på knappen **[!UICONTROL Deploy functions]** när du har fyllt i informationen.
Slutför skapandet av anslutningen genom att klicka på knappen **[!UICONTROL Save]**.

![](assets/connections_testdeploy.png){zoomable="yes"}

Du får en översikt över din Federated Database-anslutning enligt följande:

![](assets/connections_overview.png){zoomable="yes"}
