---
audience: end-user
title: Använd aktiviteten Ändra dimension
description: Lär dig hur du använder aktiviteten Ändra dimension
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Ändra dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generera ett komplement"
>abstract="Du kan generera ytterligare en utgående övergång med den återstående populationen, som har uteslutits som en dubblett. Aktivera **Generera komplement** option"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Ändra dimensionsaktivitet"
>abstract="Med den här aktiviteten kan ni ändra målgruppsdimensionen, dvs. schemat, medan ni skapar en målgrupp. Axeln flyttas beroende på datamallen och indatamängden. Du kan till exempel växla från dimensionen &quot;kontrakt&quot; till dimensionen &quot;kunder&quot;."

The **Ändra dimension** kan ni ändra målinriktningsdimensionen, dvs. schemat, medan ni skapar er målgrupp. Axeln flyttas beroende på datamallen och indatamängden. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

## Konfigurera aktiviteten Ändra dimension {#configure}

Följ de här stegen för att konfigurera **Ändra dimension** aktivitet:

1. Lägg till en **Ändra dimension** till din komposition.

   ![](../assets/change-dimension.png)

1. Definiera **Nytt schema**. Under schemaändringen sparas alla poster.

1. Kör kompositionen för att visa resultatet. Jämför data i tabellerna före och efter ändringsdimensionsaktiviteten och jämför strukturen i dispositionsregistren.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->