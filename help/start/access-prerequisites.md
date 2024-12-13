---
title: Förutsättningar och säkerhetsutkast för sammanställning av federerad publik
description: Lär dig förutsättningarna, behörigheterna och säkerhetsfunktionerna för Federated Audience Composition
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 8d498adf9f8998639e39f8f98de098682f828628
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 3%

---

# Förutsättningar och skyddsräcken {#fac-access}

Komposition för federerad publik kräver Adobe Real-time Customer Data Platform- och/eller Adobe Journey Optimizer **Prime**- eller **Ultimate**-paket. För att få tillgång till den här funktionen måste du ha köpt tillägget Federated Audience Composition.

>[!AVAILABILITY]
>
>När du har fått ett välkomstmeddelande från Adobe kan det ta några timmar innan gränssnittet har uppdaterats och funktioner är tillgängliga.

## Systemstöd {#supported-systems}

Federated Audience Composition har stöd för följande molnlager:

* Amazon Redshift
* Azure synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics

Lär dig hur du skapar en anslutning med dessa system på [den här sidan](../connections/connections.md).

<!--
## Sandboxes

When purchasing the Federated Audience Composition add-on, you are entitled to two sandboxes (one production sandbox and one non-production sandbox). For any additional sandbox provisioning requests, contact your Adobe representative.
-->

## Behörigheter {#permissions}

När du köper tillägget Federated Audience Composition skapas en produktprofil för varje aktiv sandlåda vid den tidpunkten. Den här produktprofilen skapas i Admin Console under **Adobe Experience Platform** -produktkortet och följer den här namnkonventionen: `ACP_FAC - <<SandboxName>> - admin.` Om du vill få åtkomst till Federated Audience Composition för en viss sandlåda måste användare läggas till i produktprofilen som skapats för den sandlådan.

Om till exempel en ny sandlåda med namnet &quot;fac-test&quot; aktiveras skapas en motsvarande produktprofil, &quot;ACP_FAC - fac-test - admin&quot;. För att få åtkomst till Federated Audience Composition med den här sandlådan måste användare läggas till i den här produktprofilen.

## Lista över tillåtna IP-adresser {#ip}

Om du vill aktivera Federated Audience Composition säkert för åtkomst till dina databaser måste du auktorisera IP-adresserna för de sammansättningsservrar för federerade målgrupper som ska ha åtkomst till dem. Dessa IP-adresser visas när du lägger till en federerad databas i Adobe Experience Platform användargränssnitt. [Läs mer](../connections/connections.md)

Lägg till de här IP-adresserna i tillåtelselista för att ge åtkomst till Federated Audience Composition.

## Skyddsritningar och begränsningar {#fac-guardrails}

* Federated Audience Composition är för närvarande inte tillgängligt för kunder som [har inhämtat hälsodata](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"} och för kunder som har Adobe Journey Optimizer Privacy and Security Shield. [Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Tillstånd, produktbegränsningar och prestandaskydd som anges i [Adobe Real-time Customer Data Platform-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} gäller för det här tillägget.

