---
audience: end-user
title: Översikt över aktiviteter
description: Lär dig mer om de olika aktiviteter och övergångar som är tillgängliga för användning i Federated Audience Composition.
source-git-commit: 04f4edafd1c687b94bf5617458edf0866bba16fa
workflow-type: tm+mt
source-wordcount: '4637'
ht-degree: 1%

---

# Översikt över aktiviteter

I Federated Audience Composition kan du lägga till aktiviteter och övergångar som hjälper dig att definiera målgruppen.

## Aktiviteter {#activities}

Med hjälp av aktiviteter kan du definiera komponenterna inom målgruppen.

Det finns **två** olika typer av aktiviteter som kan användas i Federated Audience Composition: målinriktningsaktiviteter och flödeskontrollaktiviteter.

### Aktiviteter för målgruppsanpassning {#targeting}

Med målinriktade aktiviteter kan ni definiera vad som utgör målgruppen för kompositionen.

#### Bygg målgrupper

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Målgrupp"
>abstract="Välj målgrupp."

Med aktiviteten **Skapa målgrupp** kan du definiera målpopulationen för kompositionen. Du kan antingen välja en befintlig målgrupp eller använda frågemodelleraren för att definiera en egen fråga.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Skapa målgrupp** på kompositionsytan ger du målgruppen ett namn. Du kan nu ange om du vill skapa en målgrupp eller använda en befintlig.

>[!BEGINTABS]

>[!TAB Skapa ny publik]

När du har valt **Skapa målgrupp** väljer du **Schema** för målgruppen. Med schemat kan du definiera målgruppen för operationen, till exempel mottagare, mottagare, operatorer eller prenumeranter. Som standard väljs schemat bland mottagarna.

![](./assets/activities/build-audience-create.png)

När du har valt ett schema väljer du **Fortsätt**. Nu kan du definiera målgruppens definition i Query Modeler. Mer information om hur du använder Query Modeler finns i [Query Modeler-översikten](../query/home.md).

>[!TAB Använd befintlig målgrupp]

När du har valt **Läs målgruppen** väljer du **Fortsätt**.

![](./assets/activities/build-audience-read.png)

Nu kan du välja vilken målgrupp du vill använda för din komposition.

>[!ENDTABS]

När du har valt dina alternativ kan du välja att **generera en utgående övergång**. Om du väljer det här alternativet kan du lägga till en utgående övergång som aktiveras i slutet av aktivitetens körning om målgruppspopulationen är tom.

+++

#### Ändra datakälla

Med aktiviteten **Ändra datakälla** kan du ändra vilken datakälla som används i kompositionen.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Ändra datakälla** på kompositionens arbetsyta kan du definiera den datakälla som ska användas för kompositionen.

![Alternativet för datakälla är markerat på arbetsytan för sammanställning av externa målgrupper.](./assets/activities/configure.png){zoomable="yes"}{width="70%"}

| Källa | Beskrivning |
| ------ | ----------- |
| Externt FDA-konto | En extern molndatabas som är ansluten till Federated Audience Composition. |

När du har valt **[!UICONTROL FDA external account]** kan du välja vilket externt konto du vill ansluta till.

![Den som visar alternativ för det externa kontot visas.](./assets/activities/fda-external-account.png){zoomable="yes"}{width="70%"}

+++

#### Ändra dimension

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generera ett komplement"
>abstract="Du kan generera ytterligare en utgående övergång med den återstående populationen, som har uteslutits som en dubblett. Aktivera alternativet **[!UICONTROL Generate complement]** om du vill göra det"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Ändra dimensionsaktivitet"
>abstract="Med den här aktiviteten kan du ändra schemat, även kallat målgruppsdimension, när du skapar en målgrupp. Axeln flyttas beroende på datamallen och indatabildschemat. Du kan till exempel växla från&quot;kontrakt&quot;-schemat till&quot;klienter&quot;-schemat."

Med aktiviteten **Ändra dimension** kan du ändra schemat (kallas även måldimension) för din komposition.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Ändra dimension** på kompositionens arbetsyta kan du definiera ett nytt schema som ersätter det tidigare schemat. Under den här schemaändringen sparas alla poster.

![](./assets/activities/change-dimension.png)

När du har kört kompositionen uppdateras resultatet.

+++

#### Kombinera

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Kombinera aktivitet"
>abstract="Med aktiviteten **Kombinera** kan du utföra segmentering på den inkommande populationen. Du kan alltså kombinera flera populationer, exkludera delar av dem eller bara behålla data som är gemensamma för flera mål."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Sammanfogningsalternativ för skärningar"
>abstract="Med **skärningspunkten** kan du bara behålla element som är gemensamma för de olika inkommande populationerna i aktiviteten. I avsnittet **Uppsättningar att gå med i** markerar du alla tidigare aktiviteter som du vill gå med i."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Alternativ för uteslutningssammanslagning"
>abstract="Med **Uteslutning** kan du utesluta element från en population enligt vissa villkor. I avsnittet **Uppsättningar att gå med i** markerar du alla tidigare aktiviteter som du vill gå med i."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Välj segmenteringstyp"
>abstract="Välj hur du vill kombinera målgrupper: union, skärning eller uteslutning."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Avstämningsalternativ för skärningar"
>abstract="Välj avstämningstypen för att definiera hur dubbletter hanteras."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Avstämningsalternativ"
>abstract="Välj **Avstämningstypen** för att definiera hur dubbletter ska hanteras."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Uteslutningsregler"
>abstract="Vid behov kan du ändra inkommande tabeller. Om du vill utesluta ett mål från ett annat schema, som också kallas måldimension, måste det här målet återställas till samma schema som huvudmålet. Om du vill göra det väljer du **Lägg till en regel** i avsnittet E **xklusionsregler** och anger villkoren för schemaändring. Datavstämning utförs antingen via ett attribut eller en koppling."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Markera uppsättningar som ska kombineras"
>abstract="I avsnittet **Uppsättningar att gå med i** väljer du den **primära uppsättningen** bland de inkommande övergångarna. Detta är den uppsättning från vilken element utesluts. De andra uppsättningarna matchar element innan de utesluts från den primära uppsättningen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Uteslutningsregler"
>abstract="Vid behov kan du ändra inkommande tabeller. Om du vill utesluta ett mål från ett annat schema, som också kallas måldimension, måste det här målet återställas till samma schema som huvudmålet. Om du vill göra det väljer du **Lägg till en regel** i avsnittet **Uteslutningsregler** och anger villkoren för schemaändring. Datavstämning utförs antingen via ett attribut eller en koppling."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Kombinera skapa komplementfärger"
>abstract="Växla till alternativet **Generera komplement** om du vill bearbeta den återstående populationen i en ytterligare övergång."

>[!NOTE]
>
>**Kombinera** aktivitet **måste** placeras efter en annan aktivitet och **kan inte** placeras i början av kompositionen.

Med aktiviteten **Kombinera** kan du förena flera målgrupper på olika sätt - en union, skärning eller uteslutning.

- **Union**: En union kombinerar de olika målgrupperna till en enda målgrupp. Detta motsvarar en OR-åtgärd.
- **Skärningspunkt**: En skärningspunkt kombinerar de olika målgrupperna till en enda målgrupp där endast det **delade** innehållet bevaras. Detta motsvarar en AND-åtgärd.
- **Uteslutning**: Ett undantag kombinerar de olika målgrupperna till en enda målgrupp utan de angivna exkluderingsreglerna. Detta motsvarar en XOR-åtgärd.

+++ Konfigurationsinformation

När du har lagt till flera aktiviteter i minst **två** olika grenar lägger du till aktiviteten **Kombinera** i slutet av en av grenarna. Du kan nu välja något av kombinationsalternativen - Förening, Skärning eller Uteslutning.

![](./assets/activities/combine.png)

>[!BEGINTABS]

>[!TAB Union]

![](./assets/activities/combine-union.png)

Om du väljer **Förening** måste du välja **avstämningstypen** för kombinationsaktiviteten. Med avstämningstypen kan du definiera hur dubblettposter hanteras.

- **Endast tangenter**: Om du väljer **Endast tangenter** behålls **ett**-element när flera element har samma nyckel. Du kan bara använda det här alternativet om de inkommande populationerna är homogena.
- **Ett urval av kolumner**: Om du väljer **Ett urval av kolumner** kan du definiera en lista med kolumner som datavstämning används på. Du kan välja den primära datauppsättningen som innehåller källdata, följt av kolumnerna som ska användas för kopplingen.

>[!TAB Skärningspunkt]

![](./assets/activities/combine-intersection.png)

Om du väljer **Skärning** måste du välja **Avstämningstyp** för kombinationsaktiviteten. Med avstämningstypen kan du definiera hur dubblettposter hanteras.

- **Endast tangenter**: Om du väljer **Endast tangenter** behålls **ett**-element när flera element har samma nyckel. Du kan bara använda det här alternativet om de inkommande populationerna är homogena.
- **Ett urval av kolumner**: Om du väljer **Ett urval av kolumner** kan du definiera en lista med kolumner som datavstämning används på.

När du har konfigurerat din avstämningstyp kan du även välja alternativet **Generera komplement**. När du genererar ett komplement bearbetas den återstående populationen och innehåller data **som inte** ingår i skärningen. En ytterligare utgående övergång läggs till i aktiviteten.

>[!TAB Uteslutning]

![](./assets/activities/combine-exclusion.png)

Om du väljer **Uteslutning** måste du välja **Primär uppsättning** bland dina inkommande övergångar. Detta representerar de uppsättningar från vilka elementen kommer att uteslutas.

När du har valt din primära uppsättning kan du konfigurera dina **undantagsregler**. Du kan antingen välja **Matcha efter attribut** eller **Koppla**.

När du har konfigurerat exkluderingsreglerna kan du även välja alternativet **Generera komplement**. När en komplementfärg genereras bearbetas den återstående populationen och innehåller data **som inte** ingår som en del av exkluderingen. En ytterligare utgående övergång läggs till i aktiviteten.

+++

#### Deduplicering

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Fält som identifierar dubbletter"
>abstract="I avsnittet **[!UICONTROL Fields to identify duplicates]** markerar du knappen **[!UICONTROL Add attribute]** för att ange för vilka fält identiska värden gör att dubbletter kan identifieras, t.ex. e-postadress, förnamn, efternamn osv. I fältordningen kan du ange vilka som ska behandlas först."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Dedupliceringsaktivitet"
>abstract="Med aktiviteten **Deduplicering** kan du ta bort dubbletter i resultatet av inkommande aktiviteter. Det används främst efter målinriktningsaktiviteter och före aktiviteter som tillåter användning av målinriktade data."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Generera ett komplement"
>abstract="Du kan generera ytterligare en utgående övergång med den återstående populationen, som har uteslutits som en dubblett. Aktivera alternativet **[!UICONTROL Generate complement]** om du vill göra det"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Inställningar för borttagning av dubbletter"
>abstract="Om du vill ta bort dubbletter i inkommande data definierar du dedupliceringsmetoden i fälten nedan. Som standard sparas bara en post. Du bör också välja dedupliceringsläget baserat på ett uttryck eller ett attribut. Som standard väljs den post som ska hållas utanför dubbletterna slumpmässigt."

Aktiviteten **Deduplicering** tar bort alla dubblettresultat inom målgruppen.

+++ Konfigurationsinformation

>[!NOTE]
>
>Om du har flera inkommande övergångar måste du först välja **Primär uppsättning** i listrutan.

När du har lagt till en **borttagning av dubbletter**-aktivitet kan du välja vilka fält som ska identifieras. Välj **Lägg till attribut** för att identifiera de fält där dubbletter kan förekomma.

![](./assets/activities/deduplication.png)

När du har identifierat fälten kan du konfigurera inställningarna för borttagning av dubbletter.

| Inställning | Beskrivning |
| ------- | ----------- |
| Dubbletter att behålla | Antalet dubblettposter som ska behållas. Om värdet är 0 behålls **alla** dubblettposter. |
| Dedupliceringsmetod | Den metod som används för att ta bort dubblettposterna. <ul><li>**Slumpmässig markering**: Den borttagna posten väljs slumpmässigt.</li><li>**Använder ett uttryck**: Den borttagna posten baseras på det skickade uttrycket. Du kan sortera i stigande eller fallande ordning beroende på vilka värden du vill ta bort.</li><li>**Värden som inte är tomma**: Den borttagna posten baseras på det skickade uttrycket. Poster där uttrycket inte har något värde tas bort.</li><li>**Följande lista med värdet**: Den borttagna posten baseras på det skickade fältet eller uttrycket. Du kan sortera de återstående värdena slumpmässigt, i stigande eller fallande ordning.</li></ul> |

Dessutom kan du välja alternativet **Skapa komplement**. När du genererar ett komplement bearbetas den återstående populationen och innehåller data **som inte** ingår som en del av dedupliceringen. En ytterligare utgående övergång läggs till i aktiviteten.

+++

#### Berikning

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Anrikningsaktivitet"
>abstract="Med aktiviteten **Enrichment** kan du förbättra måldata med ytterligare information från databasen. Den används ofta i en komposition efter segmenteringsaktiviteter."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Anrikningsaktivitet"
>abstract="När data för berikning har lagts till i kompositionen kan de användas i aktiviteter som lagts till efter aktiviteten **Enrichment** för att segmentera profiler i distinkta grupper baserat på deras beteenden, inställningar och val."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Länkdefinition"
>abstract="Skapa en länk mellan data i arbetstabellen och den federerade databasen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Anrikningsavstämning"
>abstract="Ange avstämningsparametrarna."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Anrikningsdata"
>abstract="Välj de data som ska användas för att berika kompositionen. Du kan välja två typer av anrikningsdata: ett enskilt anrikningsattribut från schemat, även kallat måldimension, eller en samlingslänk, som är en länk med en 1-N-kardinalitet mellan tabeller."

Med aktiviteten **Enrichment** kan du förbättra kompositionen genom att lägga till ytterligare data från din federerade databas.

Om du har konfigurerat en anslutning till Federated Audience Composition-målet kan du använda Enrichment-aktiviteten för att berika data som kommer från Adobe Experience Platform med attribut från din externa databas. [Lär dig hur du berikar Adobe Experience Platform-målgrupper med externa data](../connections/destinations.md)

+++ Konfigurationsinformation

>[!NOTE]
>
>Om du har flera inkommande övergångar måste du först välja **Primär uppsättning** i listrutan.

När du har lagt till aktiviteten **Enrichment** i kompositionen kan du välja **Lägg till anrikningsdata** för att välja vilket attribut du vill använda för att berika kompositionen. Du kan välja **Redigera uttryck** om du vill skapa ett avancerat uttryck för att välja attributet.

![](./assets/activities/enrichment.png)

+++

#### Avstämning

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Avstämningsaktivitet"
>abstract="Med aktiviteten **Avstämning** kan du definiera länken mellan data i databasen och data i en arbetstabell."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Avstämningsmarkeringsfält"
>abstract="Avstämningsmarkeringsfält"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Avstämning skapa villkor"
>abstract="Avstämning skapa villkor"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Avstämning genererar komplementtal"
>abstract="Avstämning genererar komplementtal"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Välj det nya schemat som ska användas på data. Med ett schema, som också kallas måldimension, kan du definiera målpopulationen: mottagare, appprenumeranter, operatorer, prenumeranter osv. Som standard är dispositionsschemat valt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Avstämningsregler"
>abstract="Välj avstämningsregler som ska användas för dedupliceringen. Om du vill använda attribut markerar du alternativet **Enkla attribut** och väljer käll- och målfälten. Om du vill skapa ett eget avstämningsvillkor med frågemodelleraren väljer du alternativet **Avancerade avstämningsvillkor** ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Välj måldimension"
>abstract="Välj schemat, även kallat måldimension, för inkommande data som ska stämma av med."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Behåll ej avstämda data"
>abstract="Som standard behålls ej avstämda data i den utgående övergången och är tillgängliga i arbetstabellen för framtida bruk. Inaktivera alternativet **Behåll ej avstämda data** om du vill ta bort ej avstämda data."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Avstämningsattribut"
>abstract="Markera det attribut som ska användas för att stämma av data och bekräfta."

>[!NOTE]
>
>Som standard behålls ej avstämda data i den utgående övergången och är tillgängliga i arbetstabellen för framtida bruk. Om du **inte** vill att avstämda data ska användas inaktiverar du alternativet **Behåll avstämda data**.

Med aktiviteten **Avstämning** kan du definiera länken mellan data i din federerade databas och data i en arbetstabell.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Avstämning** i din komposition kan du välja vilket schema som ska användas för avstämningen.

När du har valt schemat måste du konfigurera dina avstämningsregler. Du kan välja mellan **Enkla attribut** eller **Avancerade avstämningsvillkor**.

>[!BEGINTABS]

>[!TAB Enkla attribut]

När du har valt **Enkla attribut** väljer du **Lägg till regel**. Du kan nu konfigurera din avstämning genom att lägga till fälten **Source** och **Mål**. Fältet **Mål** motsvarar fälten i det valda schemat.

![](./assets/activities/reconciliation-rules.png)

Data kontrolleras när källan och målet är lika. Du kan lägga till fler avstämningsvillkor genom att välja **Lägg till regel**. Om flera kopplingsvillkor anges måste **alla** av dem verifieras så att data kan länkas tillsammans.

>[!TAB Avancerade avstämningsvillkor]

När du har valt **Avancerade avstämningsvillkor** väljer du **Skapa villkor**. Nu kan du skapa ett eget avstämningsvillkor med frågemodelleraren. Mer information om hur du använder Query Modeler finns i [Query Modeler-översikten](../query/home.md)

![](./assets/activities/reconciliation-advanced.png)

>[!ENDTABS]

Du kan även filtrera avstämda data. Välj **Skapa filter** om du vill skapa ett anpassat villkor med hjälp av Query Modeler. Mer information om hur du använder Query Modeler finns i [Query Modeler-översikten](../query/home.md)

+++

#### Spara målgrupp

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Spara en publik"
>abstract="Använd den här aktiviteten för att skapa en ny målgrupp från populationen som beräknas uppströms i kompositionen. De målgrupper som skapas läggs till i listan över målgrupper och är tillgängliga via menyn **Publiker** ."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Generera utgående övergång"
>abstract="Använd det här alternativet om du vill lägga till en övergång efter aktiviteten **Spara målgrupp**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Primärt identitetsfält"
>abstract="Välj den primära identitet som ska användas för profiler."
>additional-url="https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Läs mer i Experience Platform-dokumentationen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Namnutrymme för identitet"
>abstract="Välj det namnutrymme som ska användas för profiler."
>additional-url="https://experienceleague.adobe.com/sv/docs/experience-platform/identity/features/namespaces" text="Läs mer i Experience Platform-dokumentationen"

>[!IMPORTANT]
>
>Om din sandlåda använder en **datauppsättningsprioritet** ska du kontakta Adobe kundtjänst för att lägga till `Halos UPS`-datauppsättningen i din sammanfogningsprincip.
>
>Mer information om sammanfogningsprinciper finns i [översikten över sammanfogningsprinciper](https://experienceleague.adobe.com/sv/docs/experience-platform/profile/merge-policies/overview).

Med aktiviteten **Spara målgrupp** kan du skapa en målgrupp baserat på kompositionen. När målgruppen har skapats kan du använda dem i Audience Portal i Adobe Experience Platform. Mer information om hur du använder målgrupper med Federated Audience Composition finns i [publiköversikt](../start/audiences.md). Mer information om målgrupper i Experience Platform finns i [Översikt över målportalen](https://experienceleague.adobe.com/sv/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

+++ Konfigurationsinformation

>[!IMPORTANT]
>
>Målgruppens namn **måste** vara unikt i den aktuella sandlådan och kan inte ha samma namn som någon befintlig målgrupp.

När du har lagt till aktiviteten **Spara målgrupp** i kompositionen kan du ange namnet på den nya målgruppen.

![](./assets/activities/save-audience.png)

Nu kan du ange dina mappningar för att välja vilka fält du vill överföra till den nya målgruppen. Välj **Lägg till målgruppsmappning** och välj käll- och målgruppsfälten, som upprepas så många gånger som behövs.

När du har lagt till dina mappningar kan du välja den primära identiteten och namnutrymmet för att identifiera målprofilerna i databasen. Det primära identitetsfältet används för att identifiera profilerna medan identitetsnamnutrymmet fungerar som en nyckel för att identifiera identiteten.

Dessutom kan du ange att data ska förfalla för målgruppen. Med hjälp av data kan du bestämma hur många dagar efter det att målgruppsmedlemskapet upphör att gälla. Giltighetstiden för data kan vara mellan 1 och 90 dagar. Som standard är värdet 30.

+++

#### Dela

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Delad aktivitet"
>abstract="Med aktiviteten **Dela** kan du segmentera inkommande populationer i flera deluppsättningar baserat på olika urvalskriterier, t.ex. filtreringsregler eller populationsstorlek."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segment för delad aktivitet"
>abstract="Lägg till så många delmängder som du vill för att segmentera den inkommande populationen.<br/></br>När aktiviteten **Dela** körs segmenteras populationen mellan de olika delmängderna i den ordning som de läggs till i aktiviteten. Innan du påbörjar kompositionen måste du se till att du har ordnat delmängderna i den ordning som passar dig med pilknapparna."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Dela aktivitetsfilter"
>abstract="Om du vill använda ett filtreringsvillkor för delmängden väljer du **[!UICONTROL Create filter]** och konfigurerar den önskade filtreringsregeln med frågemodelleraren. Ta till exempel med profiler från den inkommande populationen vars e-postadress finns i databasen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Gräns för delad aktivitet"
>abstract="Om du vill begränsa antalet profiler som markeras av delmängden aktiverar du alternativet **[!UICONTROL Enable limit]** och anger antalet eller procentsatserna för den population som ska inkluderas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Sortering av delad aktivitet"
>abstract="När du anger en populationsgräns för en delmängd kan du rangordna de valda profilerna baserat på ett visst profilattribut i stigande eller fallande ordning. Aktivera alternativet **Aktivera sortering** om du vill göra det. Du kan till exempel begränsa en delmängd så att den endast innehåller de 50 översta profilerna med det högsta inköpspriset."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Delad generering av komplementfärg"
>abstract="När du har konfigurerat alla deluppsättningar kan du välja den återstående populationen som inte matchade någon av deluppsättningarna och inkludera dem i en ytterligare utgående övergång. Aktivera alternativet **Generera komplement** om du vill göra det."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Generera alla delmängder i samma tabell"
>abstract="Växla till det här alternativet om du vill gruppera alla delmängder i en enda utdataövergång."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Hoppa över tom övergång"
>abstract="Aktivera alternativet **[!UICONTROL Skip empty transition]** om du vill inaktivera utdataövergången för den här delmängden om den inkommande populationen är tom."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Aktivera överlappning av utdatapopulationer"
>abstract="Med alternativet **[!UICONTROL Enable overlapping of output populations]** kan du hantera populationer som tillhör flera delmängder. När rutan inte är markerad ser delningsaktiviteten till att en mottagare inte kan finnas i flera utdataövergångar, även om den uppfyller villkoren för flera delmängder. De kommer att vara i målet för den första fliken med matchande villkor. När rutan är markerad kan mottagarna hittas i flera delmängder om de uppfyller filtervillkoren. "

Aktiviteten **Dela** separerar den inkommande populationen i flera delar, beroende på angivna villkor.

+++ Konfigurationsinformation

>[!IMPORTANT]
>
>När aktiviteten **Dela** körs separeras populationen mellan de olika delmängderna i den **ordning de läggs till**. Om den första delmängden till exempel delar 70 % av den ursprungliga populationen, kommer nästa delmängd att tillämpa sina urvalskriterier på de återstående 30 %.
>
>Innan du utför kompositionen måste du se till att du har ordnat delmängderna i den ordning du vill att delningarna ska köras.

När du har lagt till aktiviteten **Dela** i kompositionen kan du nu bestämma hur du ska delsätta målgruppen. Välj **Lägg till segment** om du vill skapa olika förgreningssökvägar.

Du kan nu ange information för var och en av dessa delbanor. Du kan ge den underordnade sökvägen ett namn samt filtervillkoren. Om du vill skapa ett filtreringsvillkor väljer du **Skapa filter** och konfigurerar filtreringsregeln med hjälp av Query Modeler. Mer information om hur du använder Query Modeler finns i [Query Modeler-översikten](../query/home.md).

När du har skapat filtervillkoret kan du använda följande ytterligare regler:

- **Aktivera gräns**: Begränsar antalet profiler som kan delas upp i delmängden. Du kan ange detta som ett tal eller som en procentandel av populationen.
   - Om du aktiverar en gräns kan du även rangordna de valda profilerna baserat på ett specifikt profilattribut. Aktivera **Aktivera sortering** så kan du sortera attributen i stigande eller fallande ordning.
- **Hoppa över tom övergång**: Inaktiverar övergången om den inkommande populationen är tom.

Nu när deluppsättningarna har konfigurerats finns det ytterligare några alternativ som du kan ange.

| Alternativ | Beskrivning |
| ------- | ----------- |
| **Skapa komplement** | Skapar en utgående övergång som innehåller den återstående populationen. |
| **Aktivera överlappning av utdatapopulationer** | Om det här alternativet är aktiverat kan mottagaren **inte** finnas i flera utgående övergångar och kommer **endast** att finnas i den första utgående övergången. Om det är inaktiverat visas mottagaren **kan** i flera utgående övergångar. |
| **Generera alla delmängder i samma tabell** | Grupperar alla delmängder i en enda utgående övergång. |

+++

### Flödeskontrollaktiviteter {#flow-control}

Med flödeskontrollaktiviteter kan du definiera organisationen och samordningen av din komposition.

#### Och gå med

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join activity"
>abstract="Med aktiviteten **And-join** kan du synkronisera flera körningsgrenar i en komposition. Den aktiveras när alla föregående aktiviteter har slutförts. På så sätt kan du se till att vissa aktiviteter är slutförda innan du fortsätter att köra kompositionen."

Med aktiviteten **AND-join** kan du kombinera flera grenar i en komposition. Den här aktiviteten aktiveras bara när **alla** inkommande övergångar har aktiverats.

+++ Konfigurationsinformation

När du har lagt till flera aktiviteter i minst två olika grenar kan du lägga till aktiviteten **AND-join** i slutet av alla grenar.

![](./assets/activities/and-join.png)

I avsnittet **Sammanfogningsalternativ** kan du välja alla aktiviteter som du vill synkronisera. Dessutom kan du välja vilken inkommande övergång som ska behållas i listrutan **Primär uppsättning**.

+++

#### End

Aktiviteten **End** markerar slutet av kompositionen grafiskt och har ingen funktionell påverkan.

#### Förgrening

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork"
>title="Gaffelaktivitet"
>abstract="Med aktiviteten **Förena** kan du skapa utgående övergångar och starta flera aktiviteter samtidigt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork_transitions"
>title="Fork-aktivitetsövergångar"
>abstract="Som standard skapas två övergångar med en **Förgrening**-aktivitet. Välj knappen **Lägg till övergång** för att definiera ytterligare en utgående övergång och ange dess etikett."

Med aktiviteten **Förena** kan du skapa flera utgående övergångar som startar flera aktiviteter samtidigt.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Förgrening** i kompositionen genereras två utgående övergångar automatiskt. Du kan ge dessa utgående övergångar ett namn. Dessutom kan du välja **Lägg till övergång** om du vill lägga till en ny utgående övergång.

![](./assets/activities/fork.png)

+++

#### Schemaläggare

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Schemaläggaraktivitet"
>abstract="Med aktiviteten **Schemaläggaren** kan du schemalägga när målgruppskompositionen börjar. Denna aktivitet bör betraktas som en planerad start. Den kan bara användas som den första aktiviteten i en komposition."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Schemaläggarens giltighet"
>abstract="Du kan definiera en giltighetsperiod för schemaläggaren. Den kan vara permanent (standard) eller giltig till ett visst datum."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Alternativ för schemaläggare"
>abstract="Definiera frekvensen för schemaläggaren. Den kan köras vid ett specifikt tillfälle, en eller flera gånger per dag, vecka eller månad."

Med aktiviteten **Schemaläggaren** kan du schemalägga när kompositionens körning ska startas. Du **måste** använda detta som den första aktiviteten i kompositionen.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Schemaläggaren** i kompositionen kan du ange **exekveringsfrekvensen** för kompositionen. Alternativen är **En gång**, **Varje dag**, **Flera gånger om dagen**, **Varje vecka** och **Månadsvis**.

>[!BEGINTABS]

>[!TAB En gång]

>[!NOTE]
>
>Tiden anges till UTC.

Om du väljer **En gång** körs kompositionen bara en gång. Du kan välja datum och tid då kompositionen ska köras.

>[!TAB Dagligen]

Om du väljer **Daglig** utförs kompositionen en gång om dagen. Du kan dock ange vilken dag i månaden kompositionen ska köras under avsnittet **Dag i månaden**. Möjliga värden är **Varje dag**, **På veckodagar**, **Via en vald period** och **Valda veckodagar**.

| Dag i månaden | Beskrivning |
| ---------------- | ----------- |
| Varje dag | Dispositionen utförs varje dag. |
| På veckodagar | Dispositionen utförs varje veckodag. |
| Genom en vald period | Dispositionen utförs varje dag under den valda perioden. Du kan ange längden på upprepningsperioden samt datumet då perioden börjar. |
| Veckodagar | Dispositionen utförs varje dag i veckan som markeras. |

När du har valt vilken dag i månaden schemat ska köras kan du välja **Förhandsgranska starttider** för att kontrollera schemat för de kommande tio körningarna av din komposition.

>[!TAB Flera gånger om dagen]

Om du väljer **Flera gånger per dag** utförs kompositionen flera gånger per dag. Du kan välja om kompositionen ska utföras vid specifika tidpunkter per dag eller periodvis vid bestämda tidpunkter.

Om du väljer **Valda timmar** kan du välja vilka tider kompositionen ska köras. Om du väljer **Periodisk** kan du välja hur ofta kompositionen ska köras på timmar eller minuter och mellan vilka tider den ska köras. Alla tider är i UTC.

När du har valt timmar kan du välja hur ofta körningen ska köras under avsnittet **Dag i månaden**.

| Dag i månaden | Beskrivning |
| ---------------- | ----------- |
| Varje veckodag | Dispositionen utförs varje dag. |
| På vissa veckodagar | Dispositionen utförs varje dag i veckan som markeras. |

När du har valt vilken dag i månaden schemat ska köras kan du välja **Förhandsgranska starttider** för att kontrollera schemat för de kommande tio körningarna av din komposition.

>[!TAB Varje vecka]

Om du väljer **Varje vecka** utförs kompositionen med den angivna veckofrekvensen. Om du anger veckofrekvensen som ett tal som är större än 1 kan du också välja vilket datum körningen börjar.

När du har valt utvärderingsfrekvens kan du välja hur ofta körningen ska köras under avsnittet **Dag i månaden**.

| Dag i månaden | Beskrivning |
| ---------------- | ----------- |
| Varje veckodag | Dispositionen utförs varje dag. |
| På vissa veckodagar | Dispositionen utförs varje dag i veckan som markeras. |

När du har valt vilken dag i månaden schemat ska köras kan du välja **Förhandsgranska starttider** för att kontrollera schemat för de kommande tio körningarna av din komposition.

>[!TAB Månadsvis]

Om du väljer **Månadsvis** utförs kompositionen på den angivna månadsfrekvensen. Du kan antingen ange det till varje månad eller till vissa månader.

När du har valt månadsfrekvensen kan du välja **Dag i den månad** som körningen körs.

| Dag i månaden | Beskrivning |
| ---------------- | ----------- |
| Varje dag | Dispositionen utförs varje dag. |
| På veckodagar | Dispositionen utförs varje veckodag. |
| Genom en vald period | Dispositionen utförs varje dag under den valda perioden. Du kan ange längden på upprepningsperioden samt datumet då perioden börjar. |
| Veckodagar | Dispositionen utförs varje dag i veckan som markeras. |

När du har angett **Dag i månaden** kan du välja starttid. Alla tider är i UTC.

>[!ENDTABS]

När du har valt körningsfrekvens kan du välja **Giltighetsperioden** för schemat.

| Giltighetsperiod | Beskrivning |
| --------------- | ----------- |
| **Permanent (upphör aldrig)** | Kompositionen upphör aldrig att gälla. |
| **Giltighetsperiod** | Dispositionen kommer att löpa mellan de angivna datumen. |

+++

#### Vänta

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Vänta på aktivitet"
>abstract="Aktiviteten **Wait** används för att fördröja övergången från en aktivitet till en annan."

Aktiviteten **Wait** pausar kompositionens körning under den angivna tiden.

+++ Konfigurationsinformation

När du har lagt till aktiviteten **Wait** i kompositionen kan du göra den till antingen en **Varaktighet** eller en **Fast tid**-väntan.

![](./assets/activities/wait.png)

Om du väljer varaktighet kan du ange väntetiden. Denna tidsperiod kan vara i sekunder, minuter, timmar eller dagar.

Om du väljer fast tid kan du ställa in dispositionen så att den väntar till angivet datum och angiven tid. Tiden är inställd på din **lokala tidszon**.

+++

## Övergångar {#transitions}

I kompositioner visar övergångar hur data överförs från en aktivitet till en annan. Övergångarna lagrar data i en temporär arbetstabell. Om du markerar övergången kan du visa följande information:

- **Förhandsgranskningsschema**: Du kan välja det här om du vill visa arbetstabellens schema.
- **Förhandsgranska resultat**: Du kan välja det här om du vill visa data som transporteras i den valda övergången. Det här alternativet är bara tillgängligt om **Behåll resultatet av interimpopulationer mellan två körningar** är aktiverat.

![](assets/transition-preview.png)

## Nästa steg {#next-steps}

När du har läst den här guiden får du en bättre förståelse för de aktiviteter och övergångar du kan använda i en komposition. Mer information om kompositioner i allmänhet finns i [kompositionsöversikten](./create-composition.md).
