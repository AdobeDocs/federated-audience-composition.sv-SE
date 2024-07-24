---
audience: end-user
title: Använd aktiviteten Schemaläggaren
description: Lär dig hur du använder aktiviteten Schemaläggaren
exl-id: 3e8be2a2-2227-42f4-a512-b9e686ba0f66
source-git-commit: 122bd469e04d72d2dac0f606c8ab4e195100d4a4
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 7%

---

# Schemaläggare {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Schemaläggaraktivitet"
>abstract="Med aktiviteten **Schemaläggaren** kan du schemalägga när målgruppskompositionen börjar. Denna aktivitet bör betraktas som en planerad start. Den kan bara användas som den första aktiviteten i en komposition."

Aktiviteten **Schemaläggaren** är en **Flödeskontroll**-aktivitet. Du kan schemalägga när kompositionen börjar. Denna aktivitet bör betraktas som en planerad start. Den kan bara användas som den första aktiviteten i kompositionen.

Om du har konfigurerat en anslutning till Federated Data Composition-målet kan du använda den här aktiviteten för att skicka över Adobe Experience Platform-målgrupper med regelbundna intervall. [Lär dig hur du berikar Adobe Experience Platform-målgrupper med externa data](../../connections/destinations.md)

![](../assets/scheduler.png)

## Konfigurera aktiviteten Schemaläggaren {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Schemaläggarens giltighet"
>abstract="Du kan definiera en giltighetsperiod för schemaläggaren. Den kan vara permanent (standard) eller giltig till ett visst datum."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Alternativ för schemaläggare"
>abstract="Definiera frekvensen för schemaläggaren. Den kan köras vid ett specifikt tillfälle, en eller flera gånger per dag, vecka eller månad."

Följ de här stegen för att konfigurera aktiviteten **Schemaläggaren**:

1. Lägg till en **schemaläggaraktivitet** i kompositionen.

1. Konfigurera **körningsfrekvensen**:

   * **En gång**: kompositionen körs en gång.
   * **Dagligen**: Kompositionen körs vid en viss tidpunkt, en gång om dagen.
   * **Flera gånger om dagen:** Kompositionen utförs regelbundet flera gånger om dagen. Du kan ställa in körningar vid specifika tidpunkter eller med jämna mellanrum.

     >[!NOTE]
     >
     >Schemalägg inte en komposition som ska köras mer än var 15:e minut eftersom det kan påverka den totala systemprestandan negativt och skapa block i databasen.

   * **Veckovis**: Kompositionen utförs vid ett angivet tillfälle, en eller flera gånger i veckan.
   * **Månadsvis**: Kompositionen utförs vid ett angivet tillfälle, en eller flera gånger i månaden. Du kan välja månader när du vill att kompositionen ska utföras. Du kan också ställa in körningar på angivna veckodagar i månaden, till exempel den andra tisdagen i månaden.

1. Definiera körningsinformationen utifrån den valda frekvensen.  Detaljfälten kan variera beroende på vilken frekvens som används (tid, repetitionsfrekvens, angivna dagar etc.).

1. Klicka på **Förhandsgranska starttider** för att kontrollera schemat för de kommande tio körningarna av din komposition.

1. Definiera giltighetsperioden för schemaläggaren:

   * **Permanent (upphör aldrig att gälla)**: kompositionen körs enligt angiven frekvens, utan begränsningar av tidsramen eller antalet iterationer.

   * **Giltighetsperiod**: Kompositionen körs enligt angiven frekvens fram till ett visst datum. Du måste ange start- och slutdatum.

>[!NOTE]
>
>Om du vill starta kompositionen direkt kan du klicka på **Kör väntande aktivitet** i schemaläggarens övre åtgärdsfält. Den här knappen är bara tillgänglig när du har startat kompositionen.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->
