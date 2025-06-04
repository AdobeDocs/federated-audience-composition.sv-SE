---
title: Integritet och säkerhet i sammanställning av federerade målgrupper
description: Läs om hur Federated Audience Composition hanterar sekretess och säkerhet för användardata, inklusive funktioner som datastyrning, medgivande, åtkomstkontroll, datakryptering och sekretessefterlevnad.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%

---


# Integritet och säkerhet i sammanställning av federerade målgrupper

Federated Audience Composition följer ett flertal säkerhetsrutiner för att skydda data under bearbetningen.

## Integritetstjänst {#privacy}

Federated Audience Composition innehåller federerade data som Adobe Experience Platform och Adobe Journey Optimizer kan använda. Federated Audience Composition lagrar **inte** kunddata från något av datalagret. Därför kan du använda Adobe Experience Platform Privacy Service för att efterleva förfrågningar om datatradering och datatradering.

När du till exempel skapar en målgrupp med aktivitetsblocket save på arbetsytan för komposition, lagras målgruppen som en extern målgrupp i datarjön i Experience Platform. Den här externa målgruppen markeras med sitt identitetsfält och identitetsnamnutrymme. Det innebär att du kan använda Privacy Service för att komma åt och ta bort dessa profiler från en extern målgrupp.

När du har skapat en profilberikning med hjälp av aktiviteten Spara profil på arbetsytan, lagras den resulterande anrikningen i Experience Platform som ett profilaktiverat schema och profilaktiverat dataset. Den här anrikningsinformationen är markerad med ett identitetsfält och ett identitetsnamnutrymme. Därför kan du använda Privacy Service för att öppna och rensa dessa profiler.

Mer information om Privacy Service finns i [Privacy Service-översikten](https://experienceleague.adobe.com/sv/docs/experience-platform/privacy/home){target="_blank"}.

### Förfrågningar om användarens information {#privacy-requests}

I Privacy Service kan du skapa och hantera individuella sekretessförfrågningar för att få tillgång till och ta bort kunddata från Federated Audience Composition. Privacy Service tillhandahåller både ett [användargränssnitt](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=sv-SE){target="_blank"} och ett [RESTful API](https://experienceleague.adobe.com/sv/docs/experience-platform/privacy/api/overview){target="_blank"} som hjälper dig att hantera kunddataförfrågningar.

Mer information om hur du skapar och hanterar sekretessbegäranden finns i [sekretesspolicyn i Privacy Service användargränssnittshandbok](https://experienceleague.adobe.com/sv/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Bekräftelsepolicytillämpning {#consent}

Federated Audience Composition, via Experience Platform, erbjuder verktyg som gör att ni kan automatisera er medverkan i samtycket och säkerställa att ni aktiverar målgrupper baserat på det samtycke som ni har gett era kunder.

När du till exempel skapar en målgrupp med aktivitetsblocket save på arbetsytan för komposition, lagras målgruppen som en extern målgrupp i datarjön i Experience Platform. Experience Platform stöder automatiskt godkännandevalidering under aktiveringen. Mer information finns i [Vanliga frågor om segmenteringstjänsten](https://experienceleague.adobe.com/sv/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

När du har skapat en profilberikning genom att använda aktiviteten Spara profil på arbetsytan för komposition, lagras den resulterande anrikningen i Experience Platform som ett profilaktiverat schema och en profilaktiverad datauppsättning. För befintliga profiler respekteras tillgängliga medgivandeattribut automatiskt vid aktiveringen. När det gäller nya profiler respekteras automatiskt de medgivandeattribut som anges under profilåtgången under aktiveringen. Mer information om hur du tillämpar samtycke på profiler finns i [handboken för gruppen för godkännande och inställningar](https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Mer information om hur du tillämpar samtycke finns i [användargränssnittshandboken för hantering av profiler](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Datalivscykel {#data-lifecycle}

Eftersom Federated Audience Composition **inte** lagrar kunddata från något av datalagret, kan du använda Experience Platform för att hantera datalivcykeln. Med Advanced Data Lifecycle Management kan ni hantera era data-livscykler på både datauppsättnings- och postnivå.

När du till exempel skapar en målgrupp genom att använda aktivitetsblocket save på kompositionsytan, lagras den resulterande målgruppen i datarjön i Experience Platform som en extern målgrupp. Eftersom dessa data **inte** lagras i Federated Audience Composition tas målgruppsdata och motsvarande datauppsättningar automatiskt bort när målgruppen tas bort i Audience Portal.

När du har skapat en profilberikning genom att använda aktiviteten Spara profil på arbetsytan för komposition, lagras den resulterande anrikningen i Experience Platform som ett profilaktiverat schema och en profilaktiverad datauppsättning. Det innebär att du kan öppna och rensa profilerna genom att använda Datalängd.

Mer information om hur du använder datalivscykel finns i [Översikt över datalivscykler](https://experienceleague.adobe.com/sv/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Dataanvändningsetiketter {#data-usage-labels}

Med etiketter för dataanvändning kan du kategorisera datauppsättningar och fält baserat på de styrningsprinciper som gäller för dessa data. När du har skapat en målgrupp med hjälp av kompositioner kan du använda lämpliga dataetiketter i det resulterande schemat för att säkerställa att det följer de nödvändiga användningsbegränsningarna.

Mer information om hur du använder dataetiketter finns i [översikten över dataanvändningsetiketter](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Kryptering {#encryption}

Flexibel Audience Composition ger kryptering genom kryptering av data i vila, kryptering av data i transit samt kundhanterade nycklar.

Vilande data avser kunddata som används i Federated Audience Composition. Data krypteras av molntjänstleverantören och används i Federated Audience Composition i krypterad form.

Data som överförs refererar till kunddata när de flyttas från en komponent till en annan i Federated Audience Composition. Data bevaras krypterade i komponenterna för federerad målgruppskomposition med TLS 1.3 via HTTPS.

Mer information om hur Adobe hanterar datakryptering finns i handboken om [datakryptering i Experience Platform](https://experienceleague.adobe.com/sv/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Kundhanterade nycklar {#customer-managed-keys}

Med kundhanterade nycklar får du kontroll över dina data genom att du kan använda dina egna krypteringsnycklar för att kryptera dina data. Eftersom Federated Audience Composition **inte** lagrar någon kundinformation kan du använda kundhanterade nycklar direkt på målgrupperna och berikningarna, eftersom de lagras i datasjön på Experience Platform.

Mer information om kundhanterade nycklar finns i handboken [Kundhanterade nycklar](https://experienceleague.adobe.com/sv/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Granskningslogg {#audit-log}

Alla åtgärder för att skapa, läsa, uppdatera och ta bort som har utförts i Federated Audience Composition loggas i granskningsspåret. Du kan använda den här granskningsloggen för att spåra dessa åtgärder, framtvinga ansvarsskyldighet och stödja efterlevnadsrevisioner.

Mer information finns i [Översikt över granskningsspår](/help/admin/audit-trail.md){target="_blank"}.

## Åtkomstkontroll {#access-control}

Du kan styra åtkomsten till federerad målgruppskomposition på både en fält- och rollbaserad nivå. Du kan använda dessa åtkomstkontroller för att tillämpa policyer för datastyrning, begränsa exponeringen av känslig information och anpassa åtkomsten till användarnas ansvarsområden.

Mer information om åtkomstkontroll i Federated Audience Composition finns i guiden [Access Federated Audience Composition](/help/start/feature-access.md){target="_blank"}.

## Datalokalisering {#data-localization}

Sammansättning för federerad publik lagrar **inte** kunddata. Därför måste du se till att du **endast** ansluter dina externa databaser med den matchande sandlåderegionen för att behålla dina data i samma region. Om du ansluter en databas från en annan region till en sandlåda, ansvarar Adobe **inte** för datalokalisering.

## Nästa steg {#next-steps}

När du har läst den här guiden får du en bättre förståelse för de sekretess- och säkerhetsfunktioner som används för Federated Audience Composition, inklusive datastyrning, sekretess, efterlevnadskontroll, efterlevnadskontroll, livscykelhantering av data och åtkomstkontroll.
