---
audience: end-user
title: Använd aktiviteten Vänta
description: Lär dig använda aktiviteten Vänta
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 31%

---

# Vänta {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Vänta på aktivitet"
>abstract="The **Vänta** används för att fördröja övergången från en aktivitet till en annan."

The **Vänta** aktiviteten gör att det går en viss tid mellan två aktiviteter som körs. Om du till exempel vill vänta flera dagar efter en aktivitet där e-post levererats så analyserar du de öppningar och klick som genereras under den här perioden innan du utför några uppföljningsåtgärder (påminnelser via e-post, målgruppsgenerering osv.).

## Konfiguration{#wait-configuration}

Följ de här stegen för att konfigurera **Vänta** aktivitet:

1. Lägg till en **Vänta** till din komposition.

1. Ange **Varaktighet** av väntetiden mellan inkommande och utgående övergångar.

1. Välj tidsenhet i dialogrutan **Perioder** fält: sekunder, minuter, timmar, dagar.

