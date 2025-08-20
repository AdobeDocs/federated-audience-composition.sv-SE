---
audience: end-user
title: Skapa och hantera anslutningar med Federated databaser
description: Lär dig hur du skapar och hanterar anslutningar med Federated databaser
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: cc692662aa30e3263ef2da68ecd571f09c8dc6b8
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 1%

---

# Skapa anslutningar {#connections-fdb}

>[!AVAILABILITY]
>
>Du behöver en av följande behörigheter för att få åtkomst till anslutningar:
>
>-**Hantera sammanslagen databas**
>>-**Visa federerad databas**
>
>Mer information om vilka behörigheter som krävs finns i [åtkomstkontrollguiden](/help/governance-privacy-security/access-control.md).

Med Experience Platform Federated Audience Composition kan ni skapa och berika målgrupper från externa datalager och importera målgrupperna till Adobe Experience Platform.

## Databaser som stöds {#supported-databases}

Om du vill arbeta med din federerade databas och Adobe Experience Platform måste du först skapa en anslutning mellan de två källorna. Med Federated Audience Composition kan du ansluta till följande databaser.

* Amazon Redshift
* Azure Synapse Analytics
* Databricks
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

## Skapa anslutning {#create}

Om du vill skapa en anslutning väljer du **[!UICONTROL Federated databases]** i avsnittet Federated data.

![Knappen Federerade databaser är markerad i den vänstra navigeringen.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

Avsnittet Federated databaser visas. Välj **[!UICONTROL Add federated database]** om du vill skapa en anslutning.

![Knappen Lägg till federerad databas är markerad på visningssidan för Federated databaser.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

En pover för anslutningsegenskaper visas. Du kan namnge anslutningen och välja vilken typ av databas du vill skapa.

![De federerade databastyperna visas.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

När du har valt en typ visas avsnittet **[!UICONTROL Details]**. Det här avsnittet skiljer sig åt beroende på vilken databastyp som har valts tidigare.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Endast Amazon Redshift AWS, Amazon Redshift Spectrum och Amazon Redshift Serverless stöds.

När du har valt Amazon Redshift kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | Namnet på datakällan. |
| Konto | Användarnamn för kontot. |
| Lösenord | Kontots lösenord. |
| Databas | Namnet på databasen. Om detta anges i servernamnet kan fältet lämnas tomt. |
| Arbetsschema | Namnet på databasschemat som ska användas för arbetstabeller. Mer information om den här funktionen finns i [dokumentationen för Amazon-scheman](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.<br/><br/>**Obs!** Du kan använda vilket schema som helst från databasen, inklusive scheman som används för tillfällig databearbetning, så länge du har de behörigheter som krävs för att ansluta till det här schemat. Du **måste** emellertid använda distinkta arbetsscheman när du ansluter flera sandlådor med samma databas. |

>[!TAB Azure Synapse Analytics]

>[!NOTE]
>
>Om du vill skapa en säker anslutning med Azure Synapse Analytics kontaktar du Adobe kundtjänst.

När du har valt Azure Synapse Analytics kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | URL:en för Azure Synapse-servern. |
| Konto | Användarnamnet för Azure Synapse-kontot. |
| Lösenord | Lösenordet för Azure-synapskontot. |
| Databas | Namnet på databasen. Om detta anges i servernamnet kan fältet lämnas tomt. |
| Alternativ | Ytterligare alternativ för anslutningen. För Azure Synapse Analytics kan du ange vilken typ av autentisering som stöds av kopplingen. Federated Audience Composition stöder för närvarande `ActiveDirectoryMSI`. Mer information om anslutningssträngar finns i [exempelavsnittet om anslutningssträngar i Microsoft-dokumentationen](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}. |

>[!TAB Databricks]

>[!NOTE]
>
>Det finns stöd för säker åtkomst till ditt externa datalager för databanker via en privat länk. Detta inkluderar säkra anslutningar till databaser som lagras på Amazon Web Services (AWS) via privata länkar och databaser som lagras på Microsoft Azure via VPN. Kontakta Adobe om du behöver hjälp med att skapa säker åtkomst.

När du har valt Databaser kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | Namnet på databasservern. |
| HTTP-sökväg | Vägen till ditt kluster eller lagerställe. Mer information om sökvägen finns i dokumentationen för [databaser om anslutningsinformation](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Lösenord | Åtkomsttoken för databasservern. Mer information om det här värdet finns i [dokumentationen om databaser för token för personlig åtkomst](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |
| Katalog | Namnet på databankatalogen. Mer information om kataloger i databaser finns i [dokumentationen om databaser](https://docs.databricks.com/aws/en/catalogs/){target="_blank"}. |
| Arbetsschema | Namnet på databasschemat som ska användas för arbetsregistren. <br/><br/>**Obs!** Du kan använda **valfritt**-schema från databasen, inklusive scheman som används för tillfällig databearbetning, så länge du har de behörigheter som krävs för att ansluta till det här schemat. Du **måste** emellertid använda distinkta arbetsscheman när du ansluter flera sandlådor med samma databas. |
| Alternativ | Ytterligare alternativ för anslutningen. De tillgängliga alternativen visas i följande tabell. |

För databaser kan du ange följande ytterligare alternativ:

| Alternativ | Beskrivning |
| ------- | ----------- |
| TimeZoneName | Namnet på den tidszon som ska användas. Det här värdet representerar sessionsparametern `TIMEZONE`. Mer information om tidszoner finns i dokumentationen för [databaser om tidszoner](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}. |

>[!TAB Google BigQuery]

När du har valt Google BigQuery kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Tjänstkonto | E-postadressen till ditt tjänstkonto. Mer information finns i dokumentationen för [Google Cloud-tjänstkontot](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |
| Projekt | ID för ditt projekt. Mer information finns i [projektdokumentationen för Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Datauppsättning | Datauppsättningens namn. Mer information finns i [dokumentationen för Google Cloud-datauppsättningen](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Sökväg till nyckelfil | Nyckelfilen till servern. Endast `json` filer stöds. |
| Alternativ | Ytterligare alternativ för anslutningen. De tillgängliga alternativen visas i följande tabell. |

För Google BigQuery kan du ange följande ytterligare alternativ:

| Alternativ | Beskrivning |
| ------- | ----------- |
| ProxyType | Den typ av proxy som används för att ansluta till BigQuery. Värden som stöds är `HTTP`, `http_no_tunnel`, `socks4` och `socks5`. |
| ProxyHost | Värdnamnet eller IP-adressen där proxyn kan nås. |
| ProxyUid | Portnumret som proxyn körs på. |
| ProxyPwd | Lösenordet för proxyn. |
| bgpath | **Obs!** Detta gäller endast för **massinläsningsverktyget** (Cloud SDK). <br/><br/> Sökvägen till bin-katalogen i molnet för SDK på servern. Du behöver bara ange detta om du har flyttat katalogen `google-cloud-sdk` till en annan plats eller om du vill undvika att använda variabeln PATH. |
| GCloudConfigName | **Obs!** Detta gäller endast för **massinläsningsverktyget** (Cloud SDK) över version 7.3.4. <br/><br/> Namnet på konfigurationen som lagrar parametrarna för inläsning av data. Standardvärdet är `accfda`. |
| GCloudDefaultConfigName | **Obs!** Detta gäller endast för **massinläsningsverktyget** (Cloud SDK) över version 7.3.4. <br/><br/> Namnet på den tillfälliga konfigurationen som återskapar huvudkonfigurationen för inläsning av data. Standardvärdet är `default`. |
| GCloudRecreateConfig | **Obs!** Detta gäller endast för **massinläsningsverktyget** (Cloud SDK) över version 7.3.4. <br/><br/> Ett booleskt värde som gör att du kan bestämma om massinläsningsfunktionen automatiskt ska återskapa, ta bort eller ändra Google Cloud SDK-konfigurationerna. Om det här värdet är `false` läser massinläsningsmekanismen in data med en befintlig konfiguration på datorn. Om det här värdet är `true` kontrollerar du att konfigurationen är korrekt konfigurerad. Annars visas felet `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` och inläsningsmekanismen återställs till standardinläsningsmekanismen. |

>[!TAB Microsoft Fabric]

När du har valt Microsoft Fabric kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | URL:en för Microsoft Fabric-servern. |
| Program-ID | Program-ID för Microsoft Fabric. Mer information om program-ID:t finns i [Microsoft Fabric-dokumentationen om programkonfiguration](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Klienthemlighet | Klienthemligheten för programmet. Mer information om klienthemligheten finns i [Microsoft Fabric-dokumentationen om programkonfiguration](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Alternativ | Ytterligare alternativ för anslutningen. De tillgängliga alternativen visas i följande tabell. |

För Microsoft Fabric kan du ange följande ytterligare alternativ:

| Alternativ | Beskrivning |
| ------ | ----------- |
| Autentisering | Den typ av autentisering som används av kopplingen. Värden som stöds är: `ActiveDirectoryMSI`. Mer information finns i [Microsoft-dokumentationen om anslutning till lagerställe](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB Oracle]

>[!IMPORTANT]
>
>Oracle-databaskopplingen kan för närvarande **endast** användas för målgruppsskapande och målgruppsberikning.
>
>Innan du konfigurerar din Oracle-databas, inklusive ställer in din Oracle-anslutning till att använda en säker anslutning, kontaktar du Adobe kundtjänstrepresentant.

När du har valt Oracle kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | URL:en för Oracle-servern. |
| Konto | Användarnamnet för kontot. |
| Lösenord | Kontots lösenord. |

>[!TAB Snowflake]

>[!NOTE]
>
>Säker åtkomst till ditt externa Snowflake-datalager via en privat länk stöds. Observera att ditt Snowflake-konto måste ligga på Amazon Web Services (AWS) eller Azure och finnas i samma region som din Federated Audience Composition-miljö. Kontakta din Adobe-representant för att få hjälp med att konfigurera säker åtkomst till ditt Snowflake-konto.

När du har valt Snowflake kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | Serverns namn. |
| Användare | Användarnamnet för kontot. |
| Lösenord | Kontots lösenord. |
| Databas | Namnet på databasen. Om detta anges i servernamnet kan fältet lämnas tomt. |
| Arbetsschema | Namnet på databasschemat som ska användas för arbetsregistren. <br/><br/>**Obs!** Du kan använda **valfritt**-schema från databasen, inklusive scheman som används för tillfällig databearbetning, så länge du har de behörigheter som krävs för att ansluta till det här schemat. Du **måste** emellertid använda distinkta arbetsscheman när du ansluter flera sandlådor med samma databas. |
| Privat nyckel | Den privata nyckeln för databasanslutningen. Du kan överföra en `.pem`-fil från ditt lokala system. |
| Alternativ | Ytterligare alternativ för anslutningen. De tillgängliga alternativen visas i följande tabell. |

För Snowflake kan du ange följande ytterligare alternativ:

| Alternativ | Beskrivning |
| ------- | ----------- |
| arbetsschema | Namnet på databasschemat som ska användas för arbetsregister. |
| TimeZoneName | Namnet på den tidszon som ska användas. Det här värdet representerar sessionsparametern `TIMEZONE`. Som standard används systemtidszonen. Mer information om tidszoner finns i [Snowflake-dokumentationen om tidszoner](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | Den dag du vill att veckan ska börja. Det här värdet representerar sessionsparametern `WEEK_START`. Mer information om veckostart finns i [Snowflake-dokumentationen om veckans startparameter](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"} |
| AnvändCachedResult | Ett booleskt värde som avgör om Snowflake cachelagrade resultat ska användas. Det här värdet representerar sessionsparametern `USE_CACHED_RESULTS`. Som standard är det här värdet true. Mer information om den här parametern finns i [Snowflake-dokumentationen om beständiga resultat](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | Antalet trådar som ska användas för Snowflake massinläsare. Ju fler trådar som läggs till, desto bättre blir prestanda för större massladdningar. Som standard är det här värdet 1. |
| chunkSize | Filstorleken för varje gruppinläsares segment. Om du använder flera trådar samtidigt kan du förbättra prestanda för dina massinläsningar. Som standard är det här värdet 128 MB. Mer information om segmentstorlekar finns i [Snowflake-dokumentationen om hur du förbereder datafiler](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | Namnet på en företablerad intern mellanlagringsmiljö. Detta kan användas i massinläsningar i stället för att skapa en ny tillfällig fas. |

>[!TAB Vertica Analytics]

När du har valt Vertica Analytics kan du lägga till följande information:

| Fält | Beskrivning |
| ----- | ----------- |
| Server | URL:en för Vertica Analytics-servern. |
| Konto | Användarnamnet för kontot. |
| Lösenord | Kontots lösenord. |
| Databas | Namnet på databasen. Om detta anges i servernamnet kan fältet lämnas tomt. |
| Arbetsschema | Namnet på databasschemat som ska användas för arbetsregistren. <br/><br/>**Obs!** Du kan använda **valfritt**-schema från databasen, inklusive scheman som används för tillfällig databearbetning, så länge du har de behörigheter som krävs för att ansluta till det här schemat. Du **måste** emellertid använda distinkta arbetsscheman när du ansluter flera sandlådor med samma databas. |
| Alternativ | Ytterligare alternativ för anslutningen. De tillgängliga alternativen visas i följande tabell. |

För Vertica Analytics kan du ange följande ytterligare alternativ:

| Alternativ | Beskrivning |
| ------- | ----------- |
| TimeZoneName | Namnet på den tidszon som ska användas. Det här värdet representerar sessionsparametern `TIMEZONE`. Mer information om tidszoner finns i [Vertica Analytics-dokumentationen om tidszoner](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"} |

>[!ENDTABS]

Observera följande ytterligare inställningar när du har lagt till information om anslutningen:

>[!NOTE]
>
>Om du vill använda Federated Audience Composition för en viss databas måste du tillåtelselista **alla** IP-adresser som är associerade med den databasen.

| Inställningar | Information |
| -------- | ------- |
| Aktivera anslutning | Ett booleskt reglage som avgör om anslutningen aktiveras automatiskt. |
| Server-IP:n | En pover som visar vilka IP-adresser som behöver tillåtslista för att ansluta till databasen. |
| Testanslutning | Gör att du kan verifiera din konfigurationsinformation. |

Du kan nu välja **[!UICONTROL Deploy functions]** följt av **[!UICONTROL Add]** för att slutföra anslutningen mellan den federerade databasen och Experience Platform.
