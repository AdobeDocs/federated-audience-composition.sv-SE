---
audience: end-user
title: Skapa och hantera anslutningar med Federated databaser
description: Lär dig hur du skapar och hanterar anslutningar med Federated databaser
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# Skapa anslutningar {#connections-fdb}

Med Experience Platform Federated Audience Composition kan kunden bygga och berika målgrupper från tredjeparts datalager och importera målgrupperna till Adobe Experience Platform. Datalager som stöds listas i [det här avsnittet](../start/access-prerequisites.md#supported-systems).

Om du vill arbeta med din federerade databas och Adobe Experience Platform måste du först skapa en anslutning. Den här anslutningen har konfigurerats i ett dedikerat användargränssnitt som finns i Adobe Experience Platform användargränssnitt, vilket beskrivs på den här sidan.

Så här konfigurerar du en anslutning till databasen:

1. Bläddra till avsnittet **[!UICONTROL FEDERATED DATA]** i den vänstra listen.

1. Klicka på knappen **[!UICONTROL Add federated database]** i länken **[!UICONTROL Federated databases]**.

   ![](assets/connections_list.png){zoomable="yes"}

1. Ange anslutningen **[!UICONTROL Properties]** med namnet och typen för databasen.

   ![](assets/connections_name.png){zoomable="yes"}

   Om du väljer dess typ får du tillgång till andra egenskaper som du kan fylla i. Läs mer här om de databaser som stöds på [den här sidan](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   Konfigurationsinställningarna beror på typen av databas. Bläddra bland länkarna nedan för att komma åt information som du behöver för att konfigurera anslutningen:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure synapse](federated-db.md#azure-synapse-redshift)
   * [Databricks](federated-db.md#databricks)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Klicka på knappen **[!UICONTROL Test connection]** och på knappen **[!UICONTROL Deploy functions]** när du har fyllt i informationen.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

1. Slutför skapandet av anslutningen genom att klicka på knappen **[!UICONTROL Save]**.

   En översikt över din Federated-databasanslutning finns tillgänglig, vilket visas nedan:

   ![](assets/connections_overview.png){zoomable="yes"}
