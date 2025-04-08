---
title: Kom igång med Experience Platform Federated Audience Composition
description: Lär dig vad Adobe Federated Audience Composition är och hur du använder det i Adobe Experience Platform
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 3%

---

# Kom igång med Federated Audience Composition {#gs-fac}

Federated Audience Composition är tillgängligt för [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"}- och [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home){target="_blank"}-miljöer. Ni kan skapa och berika målgrupper från externa datalager och importera målgrupperna till Adobe Experience Platform. Med Federated Audience Composition får du en enkel och kraftfull lösning för att ansluta företagets datalager direkt inom Adobe Real-Time Customer Data Platform och/eller Adobe Journey Optimizer och utföra frågor i datalagrets tabeller.

Adobe Federated Audience Composition hjälper Adobe Experience Platform-appanvändare att komma åt sina kunddata som lagras i datalagret och molnlagringsplattformar som Amazon Redshift, Azure Synapse Analytics med flera. Kunddata kan lagras i flera datalager och är nu tillgängliga direkt, utan replikering. Plattformar som stöds listas på [den här sidan](../connections/federated-db.md#supported-db).

>[!INFO]
>
>Följ den här [steg-för-steg-guiden](https://experienceleague.adobe.com/en/docs/platform-learn/tutorial-comprehensive-technical/datacollection/module13/fac) för att lära dig hur du skapar målgrupper med Federated Audience Composition.

## Funktioner {#rn-capabilities}

Med Federated Audience Composition kan man utnyttja Real-Time CDP och Journey Optimizer på ett omfattande sätt:

* Utöka åtkomsten till kritiska lagerbaserade datauppsättningar för att skapa värdefulla målgrupper: Utnyttja befintliga datalager som det viktigaste systemet för register, samtidigt som ni utnyttjar förstklassiga tillämpningar för att skapa fantastiska kundupplevelser.

* Omfattande stöd för fall av strömålinriktning: Federated Audience Composition, i kombination med Real-Time CDP eller Journey Optimizer, stöder varumärkesinitierade, personaliserade upplevelser med federerade målgrupper och levererar upplevelser i realtid som triggas av händelser i realtid, kombinerat med personattribut för att uppfylla användningsbehoven i olika team.

* Minimera dataförflyttning och duplicering: Skapa målgrupper från datauppsättningar som finns i ett datalager i ett företag utan att kopiera underliggande data för att hantera användbara marknadsföringsprofiler och målgrupper.

* Använd ett enda system för upplevelsestyrda arbetsflöden: Kuratera inkapslade och federerade målgrupper i Adobe Experience Platform och koordinera utgående upplevelser i alla kanaler.

* B2C- och B2B CDP-kunder kan nu utnyttja Federated Audience Composition för att skapa personbaserade målgrupper genom att integrera data från de datalager i företaget som stöds. Dessutom kan de berika befintliga personbaserade AEP-målgrupper genom att införliva relevanta attribut som finns på företagets datalager, förbättra deras målgruppsprofiler för mer personaliserat och målinriktat engagemang.

## Användningsfall {#rn-uc}

Med ett marknadsföringsvänligt användargränssnitt kan du skapa segmentregler som söker efter en lista på de användare som är kvalificerade för ett visst segment som behövs för marknadsföringskampanjer, få tillgång till befintliga målgrupper i lagerstället för aktivering eller berika Adobe Experience Platform-målgrupper med ytterligare datapunkter som finns i lagerstället.

I den här versionen finns två exempel:

1. Målgruppsskapande: Bygg nya målgrupper utifrån företagsdatauppsättningar utan att behöva kopiera underliggande data och aktivera dessa målgrupper med färdiga destinationer.

1. Audience Enrichment: Berika befintliga målgrupper i Adobe Experience Platform genom att utnyttja sammansatta målgruppsdata som har federerats från företagets datalager. Dessa data bevaras inte i Adobe Experience Platform kundprofiler.

![diagram](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Viktiga steg {#gs-steps}

Med Adobe Federated Audience Composition kan ni skapa och uppdatera Adobe Experience Platform-målgrupper direkt från er databas, utan att behöva lägga in något material.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

Viktiga steg:

1. **Dataintegrering**: Samla data från olika källor och sammanfoga dem i en enhetlig datauppsättning. Lär dig hur du ansluter Adobe Experience Platform-program och ditt företagsdatalager, databaser som stöds och hur du konfigurerar dem finns i [det här avsnittet](../connections/federated-db.md).

1. **Datamodellering**: Designa och skapa datamodeller och scheman som definierar datastrukturen, relationerna och begränsningarna. Läs mer om scheman på [den här sidan](../customer/schemas.md). Lär dig hur du skapar länkar för din datamodell på [den här sidan](../data-management/gs-models.md).

1. **Dataomvandling**: Använd dataändringstekniker för att ändra dataelementens format, struktur eller värden så att de blir kompatibla eller lämpliga för specifika analyser eller program.

1. **Dataanvändning**: Skapa, samordna och skapa målgrupper. Lär dig hur du komponerar målgrupper på [den här sidan](../compositions/gs-compositions.md). Ni kan också uppdatera eller återanvända befintliga målgrupper via Adobe Experience Platform Audience Portal och Destinations. Läs mer på [den här sidan](../connections/destinations.md)

>[!NOTE]
>
>När kompositionen är klar sparas målgruppen i Adobe Experience Platform som en extern målgrupp och finns tillgänglig i Adobe Real-Time Customer Data Platform och/eller Adobe Journey Optimizer. Den är tillgänglig på menyn **Publiker** . [Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Styrning, integritet och säkerhet {#governance-privacy-security}

### Förfrågningar om användarens information {#gov-privacy-requests}

När du har skapat en komposition sparas målgrupperna i Adobe Experience Platform.

Du kan sedan göra sekretessförfrågningar för att få åtkomst till och/eller ta bort profildata som motsvarar dessa målgrupper via Adobe Experience Platform **Privacy Service** som tillhandahåller ett [användargränssnitt](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html){target="_blank"} och [RESTful API](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/overview){target="_blank"} som hjälper dig att hantera kunddataförfrågningar.

>[!NOTE]
>
>Mer information om Privacy Service finns i [Adobe Experience Platform-dokumentationen](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=sv){target="_blank"}.

Du kan skapa och hantera enskilda förfrågningar för att få tillgång till och ta bort kunddata från Adobe Federated Audience Composition. Stegen för att skicka **åtkomstbegäranden** och **borttagningsbegäranden** beskrivs i dokumentationen för [kundprofilen i realtid](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy){target="_blank"}.

### Granskningsspår {#gov-audit-trail}

Funktionen för granskningsspår ger en detaljerad och kronologisk redovisning av alla åtgärder och händelser som har utförts i din miljö i realtid. [Läs mer](../admin/audit-trail.md)

## Läs mer {#learn}

<!-- Workflow + Workflow activities-->


Lär dig hur du får åtkomst till federerad målgruppskomposition, skyddsutkast och begränsningar på [den här sidan](access-prerequisites.md).

Se även vanliga frågor på [den här sidan](faq.md).


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Körningsinställningar"
>abstract="I det här avsnittet kan du konfigurera inställningar som är relaterade till arbetsflödets körning, t.ex. antalet dagar som kompositionshistoriken sparas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktiviteten är inte redigerbar"
>abstract="När en **fråga** eller en **berikning**-aktivitet har konfigurerats med ytterligare data i konsolen, beaktas data för berikning och skickas till den utgående övergången, men den kan inte redigeras."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Skapa en länk"
>abstract="Definiera länkinställningarna."


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Inkrementell fråga"
>abstract="Med aktiviteten **Inkrementell fråga** kan du fråga databasen med hjälp av frågemodelleraren. Varje gång den här aktiviteten körs utesluts resultaten från tidigare körningar. På så sätt kan du bara rikta in dig på nya element."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Inkrementell frågehistorik"
>abstract="Inkrementell frågehistorik"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Inkrementell fråga Bearbetade data"
>abstract="Inkrementell fråga Bearbetade data"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="Stegvis frågeläge"
>abstract="Med den stegvisa frågan kan du köra samma fråga flera gånger genom att utesluta resultatet från tidigare körningar för varje ny körning."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Stegvis frågeläge"
>abstract="Med den stegvisa frågan kan du köra samma fråga flera gånger genom att bara ta hänsyn till resultat där datumfältet är senare än eller lika med det senaste körningsdatumet för den stegvisa frågeaktiviteten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Välj måldimension"
>abstract="Med målinriktningsdimensionen kan du definiera målgruppen för operationen: mottagare, mottagare, operatör, prenumeranter osv. Som standard väljs målet i den inbyggda tabellen Mottagare för e-post och SMS. För push-meddelanden är standardmåldimensionen prenumerantprogram."


<!-- save profile IDs-->

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Spara profil"
>abstract="Spara profil"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Spara AEP-schemalista för profil"
>abstract="Spara AEP-schemalista för profil"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepattribute"
>title="Spara profilens AEP-schemaattribut"
>abstract="Spara profilens AEP-schemaattribut"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Välj primärt identifieringsfält"
>abstract="Primärt identifieringsfält som ska användas för profiler."

>[!CONTEXTUALHELP]
>id="ddc_orchestration_saveprofile_selectdataset"
>title="AEP dataset"
>abstract="Välj den AEP-datauppsättning som ska användas för profiler."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Spara profil, välj AEP-schema"
>abstract="Välj det AEP-schema som ska användas för profiler."
