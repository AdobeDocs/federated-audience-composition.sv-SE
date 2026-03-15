---
title: Versionsinformation om sammanställning av federerad publik
description: Senaste uppdateringar och versionsinformation för Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 7d12773b36cb963f3d4251a9b88486864056a0fb
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---


# Versionsinformation

[!DNL Federated Audience Composition] levererar kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar. Alla ändringar konsolideras i versionsinformationen. [!DNL Federated Audience Composition] är inbyggt i [!DNL Adobe Experience Platform] och ärver från sina senaste innovationer och förbättringar. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## 26 februari {#fac-26-02}

Februariversionen för Federated Audience Composition har stöd för följande funktioner:

### Nya funktioner {#fac-26-02-feature}

| Stöd för fältberikning |
| --- |
| Nu kan du använda fältaktiviteten Spara i dina kompositioner. Med fältaktiviteten Spara kan du berika Experience Platform-scheman genom att federera data från externa lagerställen, så att du kan förbättra Experience Platform-scheman med ytterligare attribut. Fältaktiviteten Spara stöder både B2B- och B2C-scheman. Mer information om hur du använder den här aktiviteten finns i [aktivitetsöversikt](../compositions/activities.md#save-fields). |

| Avancerat autentiseringsstöd för databaser |
| --- |
| Du kan nu ansluta till Federated Audience Composition med Databricks med autentisering av tjänstens huvudnamn eller med OAuth 2.0. Mer information om hur du skapar en anslutning finns i [anslutningsöversikten](../connections/home.md#create). |

## 26 januari {#fac-26-01}

Januari-versionen av Federated Audience Composition har stöd för följande nya funktioner och förbättringar:

### Nya funktioner {#fac-26-01-feature}

| Stöd för Azure Synapse Service Principal Authentication |
| --- |
| Nu kan du ansluta till Federated Audience Composition med Azure Synapse via ett Service Principal. Mer information om hur du skapar en anslutning finns i [anslutningsöversikten](../connections/home.md#create). |

| Tillgänglighet för Adobe Experience Platform-kunder på Amazon Web Services (AWS) |
| --- |
| Nu kan du använda Federated Audience Composition om din Experience Platform-instans finns i AWS. Mer information om Experience Platform i AWS finns i [översikten för flera moln](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud). |

### Förbättringar {#fac-26-01-improvements}

Den här versionen innehåller följande förbättring.

- **Konfiguration för förfallodatum för data för målgrupper**

  Du kan nu ange en förfallotid för data när du använder aktiviteten **Spara målgrupp** i en komposition.

  Läs [aktivitetsguiden](../compositions/activities.md#save-audience) om du vill veta mer om dataförfallodatum i federerad publikkomposition.
