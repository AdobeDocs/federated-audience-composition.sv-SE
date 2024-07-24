---
audience: end-user
title: Använd aktiviteten Vänta
description: Lär dig använda aktiviteten Vänta
badge: label="Begränsad tillgänglighet" type="Informative"
exl-id: 59857bd2-2a0b-4c97-ba4e-048dfd9af8f2
source-git-commit: 122bd469e04d72d2dac0f606c8ab4e195100d4a4
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

---

# Vänta {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Vänta på aktivitet"
>abstract="Aktiviteten **Wait** används för att fördröja övergången från en aktivitet till en annan."

Aktiviteten **Wait** tillåter en viss tid mellan två aktiviteter som körs.

## Konfiguration{#wait-configuration}

Följ de här stegen för att konfigurera aktiviteten **Wait**:

1. Lägg till en **Vänta**-aktivitet i kompositionen.

1. Ange **Varaktighet** för väntetiden mellan inkommande och utgående övergångar.

1. Välj tidsenhet i fältet **Perioder**: sekunder, minuter, timmar, dagar.

   ![](../assets/wait.png)
