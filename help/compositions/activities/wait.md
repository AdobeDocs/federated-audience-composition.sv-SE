---
audience: end-user
title: Använd aktiviteten Vänta
description: Lär dig använda aktiviteten Vänta
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 30%

---

# Vänta {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Vänta på aktivitet"
>abstract="Aktiviteten **Wait** används för att fördröja övergången från en aktivitet till en annan."

Aktiviteten **Wait** tillåter en viss tid mellan två aktiviteter som körs. Om du till exempel vill vänta flera dagar efter en aktivitet där e-post levererats så analyserar du de öppningar och klick som genereras under den här perioden innan du utför några uppföljningsåtgärder (påminnelser via e-post, målgruppsgenerering osv.).

## Konfiguration{#wait-configuration}

Följ de här stegen för att konfigurera aktiviteten **Wait**:

1. Lägg till en **Vänta**-aktivitet i kompositionen.

1. Ange **Varaktighet** för väntetiden mellan inkommande och utgående övergångar.

1. Välj tidsenhet i fältet **Perioder**: sekunder, minuter, timmar, dagar.


