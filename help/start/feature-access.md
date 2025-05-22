---
title: Åtkomst till sammansatt målgrupp
description: Lär dig mer om nödvändiga behörigheter för Federated Audience Composition
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 7f8ba57e0fd53350690e391e015f5161b2b7d04e
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Åtkomst till sammansatt målgrupp {#feature-access}

## Hantera åtkomst till sandlådor {#access-sandboxes}

När du köper Adobe Experience Platform Federated Audience Composition skapas en produktprofil för varje aktiv sandlåda vid den tidpunkten. Den här produktprofilen skapas i Admin Console under **Adobe Experience Platform** -produktkortet och följer den här namnkonventionen: `ACP_FAC - <<SandboxName>> - admin.` Om du vill få åtkomst till Federated Audience Composition för en viss sandlåda måste användare läggas till i produktprofilen som skapats för den sandlådan.

Om till exempel en ny sandlåda med namnet &quot;fac-test&quot; aktiveras skapas en motsvarande produktprofil, &quot;ACP_FAC - fac-test - admin&quot;. För att få åtkomst till Federated Audience Composition med den här sandlådan måste användare läggas till i den här produktprofilen.

## Hantera åtkomst till sammanställning av federerad publik

Om du vill få åtkomst till **Federated Audience Composition** måste du först se till att du tilldelar de behörigheter som krävs för att få åtkomst till olika aspekter av Federated Audience Composition. Dessa roller måste sedan tilldelas användare som behöver åtkomst till **Federated Audience Composition**.

Observera att det endast är administratörer som kan tilldela behörigheter.

1. Navigera till menyn **[!UICONTROL Permissions]**.

1. Välj den **[!UICONTROL Role]** du vill uppdatera på menyn **[!UICONTROL Roles]**.

   ![](assets/access_fda_1.png)

1. Välj **[!UICONTROL Edit]** om du vill ändra rollens behörigheter.

   ![](assets/access_fda_2.png)

1. Lägg till de behörigheter som krävs för användaren. Du kan lägga till följande behörigheter för åtkomst till federerad målgruppskomposition:

   | Behörighet | Beskrivning |
   | ---------- | ----------- |
   | Hantera federerade data | Använd den här behörigheten för att hantera alla aspekter av sammanställningen för federerad publik. Behörighetsgrupperna Hantera Federate-databas, Hantera Federated schema, Hantera Federated Data Model och Hantera Federated Compositions. |
   | Hantera sammanslagen databas | Använd den här behörigheten för att lägga till, visa, uppdatera och ta bort anslutningar till federerade databaser. |
   | Visa federerad databas | Använd den här behörigheten för att visa dina anslutningar till federerade databaser. |
   | Hantera federerat schema | Använd den här behörigheten för att skapa, visa, uppdatera, ta bort och uppdatera scheman. |
   | Visa data för federerat schema | Använd den här behörigheten för att visa fliken Data i schemaavsnittet. |
   | Visa federerat schema | Använd den här behörigheten för att visa schematabellerna. |
   | Hantera sammanslagen datamodell | Använd den här behörigheten för att skapa, visa, uppdatera och ta bort datamodeller. |
   | Visa federerad datamodell | Använd den här behörigheten för att visa datamodeller. |
   | Visa federationsgranskningsspår | Använd den här behörigheten om du vill visa granskningsspår för federerad målgruppskomposition. |
   | Hantera sammanslagna kompositioner | Använd den här behörigheten för att skapa, visa, uppdatera och ta bort federerade kompositioner. |
   | Visa federerade kompositioner | Använd den här behörigheten för att visa externa kompositioner. |

   ![](assets/permissions.png)

1. När du har gjort de nödvändiga ändringarna väljer du **[!UICONTROL Save]**.

Alla användare som redan är tilldelade den här rollen får sina behörigheter automatiskt uppdaterade och tillgång till Federated Audience Composition.

Så här tilldelar du rollen till nya användare:

1. Navigera till fliken **[!UICONTROL Users]** på din rollkontrollpanel och välj **[!UICONTROL Add Users]**.

   ![](assets/access_fda_4.png)

1. Ange användarens namn eller e-postadress eller välj i listan över tillgängliga. Välj **[!UICONTROL Save]** när du är klar.

Du kan också tilldela en av de befintliga rollerna till användarna, beroende på vilka behörigheter de behöver. Mer information om hur du tilldelar befintliga roller till en användare finns i [handboken om hur du hanterar användare för en produktprofil](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/ui/users).

| Rollnamn | Behörigheter |
| --------- | ----------- |
| Vanliga datahanterare | <ul><li>Hantera sammanslagna kompositioner</li><li>Visa federerade databaser</li><li>Visa sammanfogade scheman</li><li>Visa data för federerat schema</li><li>Visa federerade datamodeller</li></ul> |
| FAC Composition Managers | <ul><li>Hantera sammanslagna kompositioner</li></ul> |
| Administratörer för vanliga frågor | <ul><li>Hantera federerade data</li></ul> |

Användaren får sedan ett e-postmeddelande med instruktioner om hur man kommer åt instansen. Om användaren inte har skapats tidigare, se [den här dokumentationen](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/abac/permissions-ui/users).
