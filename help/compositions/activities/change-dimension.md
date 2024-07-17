---
audience: end-user
title: Använd aktiviteten Ändra dimension
description: Lär dig hur du använder aktiviteten Ändra dimension
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Ändra dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generera ett komplement"
>abstract="Du kan generera ytterligare en utgående övergång med den återstående populationen, som har uteslutits som en dubblett. Aktivera alternativet **[!UICONTROL Generate complement]** om du vill göra det"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Ändra dimensionsaktivitet"
>abstract="Med den här aktiviteten kan du ändra schemat, även kallat målgruppsdimension, när du skapar en målgrupp. Axeln flyttas beroende på datamallen och indatabildschemat. Du kan till exempel växla från&quot;kontrakt&quot;-schemat till&quot;klienter&quot;-schemat."

Med aktiviteten **Ändra dimension** kan du ändra schemat, som också kallas måldimension, när du skapar din målgrupp. Axeln flyttas beroende på datamallen och indatabildschemat.

## Konfigurera aktiviteten Ändra dimension {#configure}

Följ de här stegen för att konfigurera aktiviteten **Ändra dimension**:

1. Lägg till en **Ändra dimension**-aktivitet i kompositionen.

   ![](../assets/change-dimension.png)

1. Definiera det **nya schemat**. Under schemaändringen sparas alla poster.

1. Kör kompositionen för att visa resultatet. Jämför data i tabellerna före och efter aktiviteten **Ändra dimension** och jämför strukturen i dispositionstabellerna.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->