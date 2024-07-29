---
title: Åtkomst till sammansatt målgrupp
description: Lär dig hur du får åtkomst till sammanställningen för federerade målgrupper.
badge: label="Begränsad tillgänglighet" type="Informative"
source-git-commit: 618d1675c28213d7a316f40cd624d282e01297f1
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Åtkomst till sammansatt målgrupp {#fac-access}

## Paket och tillägg {#package}

Federated Audience Composition kräver Adobe Real-time Customer Data Platform- och Adobe Journey Optimizer Prime- eller Ultimate-paket. För att få tillgång till den här funktionen måste du ha köpt tillägget Federated Audience Composition.

>[!AVAILABILITY]
>
>När du har fått ett välkomstmeddelande från Adobe kan det ta några timmar innan gränssnittet har uppdaterats och funktioner är tillgängliga.

## Behörigheter {#permissions}

När du köper tillägget Federated Audience Composition skapas en produktprofil för varje aktiv sandlåda vid den tidpunkten. Den här produktprofilen skapas i Admin Console under **Adobe Experience Platform** -produktkortet och följer den här namnkonventionen: `ACP_FAC - <<SandboxName>> - admin.` Om du vill få åtkomst till Federated Audience Composition för en viss sandlåda måste användare läggas till i produktprofilen som skapats för den sandlådan.

Om till exempel en ny sandlåda med namnet &quot;fac-test&quot; aktiveras skapas en motsvarande produktprofil, &quot;ACP_FAC - fac-test - admin&quot;. För att få åtkomst till Federated Audience Composition med den här sandlådan måste användare läggas till i den här produktprofilen.

## Lista över tillåtna IP-adresser {#ip}

Dina IP-adresser måste läggas till i tillåtelselista för att du ska kunna få åtkomst till ditt datalager och använda Federated Audience Composition. Om du vill lägga till dina IP-adresser i tillåtelselista kontaktar du Adobe.

## Skyddsritningar och begränsningar {#fac-guardrails}

* Federated Audience Composition är kompatibelt med Privacy &amp; Security Shield och kan användas i alla vertikaler utom för hälso- och sjukvårdsbranscher. För närvarande kan Federated Audience Composition inte licensieras till kunder som vill importera hälsodata. [Läs mer](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* Tillstånd, produktbegränsningar och prestandaskydd som anges i [Adobe Real-time Customer Data Platform-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} gäller för det här tillägget.
