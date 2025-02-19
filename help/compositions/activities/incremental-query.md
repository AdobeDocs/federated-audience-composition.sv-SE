---
audience: end-user
title: Använd inkrementell frågeaktivitet
description: Lär dig hur du använder aktiviteten Inkrementell fråga
hide: true
hidefromtoc: true
source-git-commit: 34d6fc8f97c491fcb91eebf8e1377018e5020a4a
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 15%

---

# Inkrementell fråga {#incremental-query}

<!-- Warning : contextual help IDs are declared in /start/get-started.md-->

Med aktiviteten **Inkrementell fråga** kan du fråga databasen på schemalagd basis. Varje gång den här aktiviteten körs utesluts resultaten från tidigare körningar. På så sätt kan du bara rikta in dig på nya element.

Aktiviteten **[!UICONTROL Incremental query]** kan användas för olika typer av användning:

* Segmentera individer för att definiera målet för ett meddelande, en målgrupp osv.
* Exporterar data. Du kan till exempel använda aktiviteten för att regelbundet exportera nya loggar i filer. Det kan vara användbart om du vill använda dina loggdata i externa rapporterings- eller BI-verktyg.

Den population som tidigare körningar redan har som mål lagras i kompositionen. Det innebär att två kompositioner som startats från samma mall inte delar samma logg. Två uppgifter som baseras på samma inkrementella fråga i samma disposition använder dock samma logg.

Om resultatet av en stegvis fråga är lika med 0 under en av körningarna pausas kompositionen tills frågan körs nästa gång. De övergångar och aktiviteter som följer efter den stegvisa frågan bearbetas därför inte före nästa körning.

## Konfigurera aktiviteten Inkrementell fråga {#incremental-query-configuration}

Följ de här stegen för att konfigurera aktiviteten **Inkrementell fråga**:

1. Lägg till en **inkrementell frågeaktivitet** i din komposition.

1. I avsnittet **[!UICONTROL Audience]** väljer du **Måldimension** och klickar sedan på **[!UICONTROL Continue]**.

   Med målinriktningsdimensionen kan du definiera målgruppen för operationen: mottagare, mottagare, operatör, prenumeranter osv. Som standard är målet markerat bland mottagarna. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Använd frågemodelleraren för att definiera frågan, på samma sätt som du skapar en målgrupp när du utformar ett nytt e-postmeddelande. [Lär dig arbeta med frågemodelleraren](../../query/query-modeler-overview.md)

1. I avsnittet **[!UICONTROL Processed data]** väljer du det inkrementella läge som ska användas:

   * **[!UICONTROL Exclude results of previous execution]**: Varje gång aktiviteten körs exkluderas resultatet från tidigare körningar.

     Poster som redan har valts i tidigare körningar kan loggas i högst ett antal dagar från den dag de angavs som mål. Använd fältet **[!UICONTROL History in days]** om du vill göra det. Om värdet är noll rensas mottagarna aldrig från loggen.

   * **[!UICONTROL Use a date field]**: Med det här alternativet kan du exkludera resultat från tidigare körningar baserat på ett specifikt datumfält. Det gör du genom att välja önskat datumfält i listan över tillgängliga attribut för den valda måldimensionen. Vid nästa körning av kompositionen hämtas endast data som har ändrats eller skapats efter det senaste körningsdatumet.

     Efter den första körningen av kompositionen blir fältet **[!UICONTROL Last execution date]** tillgängligt. Det anger vilket datum som ska användas för nästa körning och uppdateras automatiskt varje gång kompositionen körs. Du kan fortfarande åsidosätta det här värdet genom att ange ett nytt värde manuellt så att det passar dina behov.

   >[!NOTE]
   >
   >**[!UICONTROL Use a date field]**-läget ger större flexibilitet beroende på vilket datumfält som är markerat. Om det angivna fältet till exempel motsvarar ett ändringsdatum, kan du i datumfältsläget hämta data som nyligen uppdaterats, medan det andra läget helt enkelt utelämnar inspelningar som redan har valts i en tidigare körning, även om de har ändrats sedan den senaste kompositionen.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
