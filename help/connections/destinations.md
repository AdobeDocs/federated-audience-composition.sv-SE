---
audience: end-user
title: Skicka målgrupper till Adobe Federated Audience Composition
description: Lär dig hur du skickar Adobe Experience Platform-målgrupper till Federated Audience Composition
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 1e400d98040cdbcc6f13f84faa00e8efa6cfbd4a
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Skicka Adobe Experience Platform till Adobe Federated Audience Composition {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Skapa ett mål"
>abstract="Ange inställningarna för att ansluta till den nya Federated Database. Använd knappen **[!UICONTROL Connect to destination]** för att validera konfigurationen."

Med Adobe Experience Platform kan ni skicka över målgrupper från Audience-portalen till Adobe Federated Audience Composition. På så sätt kan ni utnyttja befintliga målgrupper i kompositioner och kombinera dem med data från externa databaser för att skapa nya eller uppdatera befintliga målgrupper.

För att göra det måste du skapa en ny anslutning i Adobe Experience Platform till Adobe Federated Audience Composition-målet. Du kan använda en schemaläggare för att skicka en viss målgrupp med regelbundna intervall och välja vilka fält som ska skickas med målgruppen, till exempel ID:n för avstämning av data. Om ni har tillämpat styrnings- och integritetspolicyer på er målgrupp kommer de att behållas och skickas tillbaka till målgruppsportalen när målgruppen har uppdaterats.

De viktigaste stegen för att skicka Adobe Experience Platform-målgrupper till Adobe Federated Audience Composition är följande:

1. Gå till Adobe Experience Platform destinationskatalog och välj mål för federerad målgruppskomposition.

   Välj **[!UICONTROL Configure new destination]** i den högra rutan.

   ![](assets/destination-new.png)

1. Ange ett namn för den nya anslutningen, välj den **[!UICONTROL Connection type]** som ska användas och den **[!UICONTROL Federated database]** som du vill ansluta till och klicka på **[!UICONTROL Next]**.

   ![](assets/destination-configure.png)

   I avsnittet **[!UICONTROL Alerts]** kan du aktivera aviseringar för att få meddelanden om dataflödets status till ditt mål. Mer information om varningar finns i guiden [prenumerera på destinationsvarningar med användargränssnittet](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts).

1. I steget **[!UICONTROL Governance policy & enforcement actions]** kan du definiera dina datastyrningsprinciper och se till att de data som används är kompatibla när målgrupper skickas och är aktiva.

   När du är klar med att välja önskade marknadsföringsåtgärder för målet klickar du på **[!UICONTROL Create]**.

1. Den nya anslutningen till målet skapas. Nu kan du aktivera målgrupper att skicka över till målet. Om du vill göra det markerar du den i listan och klickar på **[!UICONTROL Next]**

   ![](assets/destination-activate.png)

1. Markera önskade målgrupper som du vill skicka och klicka på **[!UICONTROL Next]**.

1. Konfigurera filnamnet och ett exportschema för de valda målgrupperna.

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Detaljerad information om hur du konfigurerar schema och filnamn finns i Adobe Experience Platform-dokumentationen:
   >* [Schemalägg målgruppsexport](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling)
   >* [Konfigurera filnamn](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names)

1. I steget **[!UICONTROL Mapping]** väljer du vilka attribut- och identitetsfält som ska exporteras för målgruppen/målgrupperna. Mer information finns i [mappningssteget](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping) i Adobe Experience Platform-dokumentationen.

   ![](assets/destination-attributes.png)

1. Granska målkonfigurationen och målgruppsinställningarna och klicka sedan på **[!UICONTROL Finish]**.

   ![](assets/destination-review.png)

De valda målgrupperna är nu aktiverade för den nya anslutningen. Du kan lägga till fler målgrupper att skicka med den här anslutningen genom att gå tillbaka till sidan **[!UICONTROL Activate audiences]**. Du kan inte ta bort målgrupper när de har aktiverats.
