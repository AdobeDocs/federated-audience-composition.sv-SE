---
audience: end-user
title: Skapa din första fråga med frågemodelleraren
description: Lär dig hur du skapar din första fråga i frågemodelleraren.
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '2092'
ht-degree: 52%

---

# Redigera uttryck {#expression}

När du redigerar ett uttryck måste du ange villkor manuellt för att skapa en regel. I det här läget kan du använda avancerade funktioner som gör att du kan ändra de värden som används för att utföra specifika frågor, som att ändra datum, strängar, numeriska fält, sortering osv.

>[!IMPORTANT]
>
>Avsnittet nedan innehåller information om hur du arbetar med uttrycksredigeraren för att skapa regler. Tänk på att den syntax som används för att skapa regler skiljer sig från den som används för att lägga till personalisering.

## Arbeta med uttrycksredigeraren {#edit}

Uttrycksredigeraren är tillgänglig från frågemodelleraren **[!UICONTROL Edit expression]** knapp, tillgänglig för **[!UICONTROL Attribute]** och **[!UICONTROL Value]** fält när du konfigurerar ett anpassat villkor.

| Åtkomst från **Attribut** fält | Åtkomst från **Värde** fält |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

Uttrycksredigeraren innehåller:

* An **inmatningsfält (1)** som uttrycket är definierat i.
* Listan med tillgängliga **fält (2)** som kan användas i uttrycket och som motsvarar schemat, även kallat måldimension, för frågan.
* **Hjälpfunktioner (3)**, sorterat efter kategori.

Redigera uttrycket genom att ange ett uttryck direkt i indatafältet. Om du vill lägga till ett fält eller en hjälpfunktion placerar du markören i uttrycket där du vill lägga till det och klickar på plusknappen.

![](assets/expression-editor.png){zoomable="yes"}

När uttrycket är klart klickar du på **[!UICONTROL Confirm]** -knappen. Uttrycket visas i det markerade fältet. Om du vill redigera den öppnar du uttrycksredigeraren och gör önskade ändringar.

I exemplet nedan visas ett uttryck som konfigurerats för **[!UICONTROL Value]** fält. Om du vill redigera den måste du öppna uttrycksredigeraren med **[!UICONTROL Edit expression]** -knappen.

![](assets/edit-expression-value.png){zoomable="yes"}

## Hjälpfunktioner

Med frågeredigeringsverktyget kan du använda avancerade funktioner för att utföra komplex filtrering beroende på önskade resultat och typer av manipulerade data. Följande funktioner är tillgängliga:

### Sammanställd

Sammanställningsfunktionerna används för att utföra beräkningar på en uppsättning värden.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Genomsnittlig</strong><br /> </td> 
   <td> Returnerar medelvärdet för en taltypskolumn<br /> </td> 
   <td> Avg(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Antal</strong><br /> </td> 
   <td> Räknar värden som inte är null i en kolumn<br /> </td> 
   <td> Count(&lt;value&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>CountAll</strong><br /> </td> 
   <td> Räknar returnerade värden (alla fält)<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Motdistinkt</strong><br /> </td> 
   <td> Räknar de distinkta icke-null-värdena för en kolumn<br /> </td> 
   <td> CountDict(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Max</strong><br /> </td> 
   <td> Returnerar det maximala värdet för en kolumn av typen tal, sträng eller datum<br /> </td> 
   <td> Max(&lt;value&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Min</strong><br /> </td> 
   <td> Returnerar det minsta värdet för en kolumn av typen tal, sträng eller datum<br /> </td> 
   <td> Min(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>StdDev</strong><br /> </td> 
   <td> Returnerar standardavvikelsen för ett tal, en sträng eller en datumkolumn<br /> </td> 
   <td> StdDev(&lt;value&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>StringAgg</strong><br /> </td> 
   <td> Returnerar sammanfogningen av värdena i en strängtypskolumn, avgränsade med tecknet i det andra argumentet<br /> </td> 
   <td> StringAgg(&lt;value&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Summa</strong><br /> </td> 
   <td> Returnerar summan av värdena för en kolumn av typen tal, sträng eller datum<br /> </td> 
   <td> Sum(&lt;value&gt;)<br /></td> 
  </tr> 
 </tbody> 
</table>

### Datum

Datumfunktionerna används för att ändra datum- och tidsvärden.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> Lägger till ett antal dagar till ett datum<br /> </td> 
   <td> AddDays(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> Lägger till ett antal timmar till ett datum<br /> </td> 
   <td> AddHours(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> Lägger till ett antal minuter till ett datum<br /> </td> 
   <td> AddMinutes(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> Lägger till ett antal månader till ett datum<br /> </td> 
   <td> AddMonths(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> Lägger till ett antal sekunder till ett datum<br /> </td> 
   <td> AddSeconds(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> Lägger till ett antal år till ett datum<br /> </td> 
   <td> AddYears(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>ConvertNTZ</strong><br /> </td> 
   <td> Konverterar tidsstämpeln NTZ (tidsstämpel utan tidszon) till TZ (tidsstämpel med tidszon) med definierad session-TZ<br/> </td> 
   <td> ConvertNTZ (&lt;date time=""&gt;)<br /> </td>  
  </tr>
  <tr> 
   <!--<td> <strong>ConvertTimezone</strong><br /> </td> 
   <td> <br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;)<br /> </td>  
  </tr>-->
  <tr> 
   <td> <strong>DateCmp</strong><br /> </td> 
   <td> Jämför två datum<br/> </td> 
   <td> DateCmp(&lt;date&gt;,&lt;date&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> Returnerar endast datumet (med tiden 00:00)*<br /> </td> 
   <td> DateOnly(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> Returnerar talet som representerar dagen på datumet<br /> </td> 
   <td> Day(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> Returnerar numret på dagen i datumåret<br /> </td> 
   <td> DayOfYear(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> Returnerar det datum som motsvarar aktuellt datum minus n dagar<br /> </td> 
   <td> DaysAgo(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> Returnerar det datum (heltal åååmmdd) som motsvarar det aktuella datumet minus n dagar<br /> </td> 
   <td> DaysAgoInt(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> Antal dagar mellan två datum<br /> </td> 
   <td> DaysDiff(&lt;slutdatum&gt;, &lt;startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> Returnerar åldern i dagar för ett datum<br /> </td> 
   <td> DaysOld(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> Returnerar serverns aktuella systemdatum<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> Returnerar timmen för datumet<br /> </td> 
   <td> Hour(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> Returnerar antalet timmar mellan två datum<br /> </td> 
   <td> HoursDiff(&lt;slutdatum&gt;, &lt;startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> Returnerar minuterna av datumet<br /> </td> 
   <td> Minute(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> Returnerar antalet minuter mellan två datum<br /> </td> 
   <td> MinutesDiff(&lt;slutdatum&gt;, &lt;startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> Returnerar talet som representerar månaden för datumet<br /> </td> 
   <td> Month(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> Returnerar det datum som motsvarar aktuellt datum minus n månader<br /> </td> 
   <td> MonthsAgo(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> Returnerar antalet månader mellan två datum<br /> </td> 
   <td> MonthsDiff(&lt;slutdatum&gt;, &lt;startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> Returnerar åldern i månader för ett datum<br /> </td> 
   <td> MonthsOld(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> Returnerar det äldsta datumet i ett intervall<br /> </td> 
   <td> Äldst (&lt;date date=""&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> Returnerar sekunder för datumet<br /> </td> 
   <td> Second(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> Returnerar antalet sekunder mellan två datum<br /> </td> 
   <td> SecondsDiff(&lt;slutdatum&gt;, &lt;startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> Subtraherar ett antal dagar från ett datum<br /> </td> 
   <td> SubDays(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> Subtraherar ett antal timmar från ett datum<br /> </td> 
   <td> SubHours(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> Subtraherar ett antal minuter från ett datum<br /> </td> 
   <td> SubMinutes(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> Subtraherar ett antal månader från ett datum<br /> </td> 
   <td> SubMonths(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> Subtraherar ett antal sekunder från ett datum<br /> </td> 
   <td> SubSeconds(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> Subtraherar ett antal år från ett datum<br /> </td> 
   <td> SubYears(&lt;datum&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> Konverterar ett datum + tid som ett datum<br /> </td> 
   <td> ToDate(&lt;datum + tid&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> Konverterar en sträng till ett datum + tid<br /> </td> 
   <td> ToDateTime(&lt;sträng&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToTimestamp</strong><br /> </td> 
   <td> Konverterar en sträng till en tidsstämpel<br /> </td> 
   <td> ToTimestamp()&lt;string&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToTimeZone</strong><br /> </td> 
   <td> Konvertera ett datum + tid till en tidszon<br /> </td> 
   <td> ToTimeZone(&lt;date&gt;,&lt;time zone=""&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> Avrundar ett datum + tid till närmaste sekund<br /> </td> 
   <td> TruncDate(@lastModified, &lt;antal sekunder&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> Avrundar ett datum + tid till en viss precision, uttryckt i sekunder<br /> </td> 
   <td> TruncDateTZ(&lt;datum&gt;, &lt;antal sekunder&gt;, &lt;tidszon&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> Avrundar ett datum till kvartal<br /> </td> 
   <td> TruncQuarter(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> Avrundar tidsdelen upp till närmaste sekund<br /> </td> 
   <td> TruncTim(e)&lt;date&gt;, &lt;number of="" seconds=""&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> Avrundar ett datum till veckan<br /> </td> 
   <td> TruncWeek(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> Avrundar ett datum + tid till 1 januari under året<br /> </td> 
   <td> TruncYear(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> Returnerar ett tal som representerar dagen i veckan på datumet (0=måndag, 6=söndag)<br /> </td> 
   <td> WeekDay(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> Returnerar talet som representerar datumåret<br /> </td> 
   <td> Year(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearAnd Month</strong><br /> </td> 
   <td> Returnerar talet som representerar året och månaden på datumet<br /> </td> 
   <td> YearAndMonth(&lt;datum&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>ÅrFörÅR</strong><br /> </td> 
   <td> Returnerar antalet år mellan ett givet datum och det aktuella datumet<br /> </td> 
   <td> YearsAgo(&lt;date&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsDiff</strong><br /> </td> 
   <td> Returnerar antalet år mellan de två datumen<br /> </td> 
   <td> YearsDiff(&lt;slutdatum&gt;, &lt;startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> Returnerar åldern i år för ett datum<br /> </td> 
   <td> YearsOld(&lt;datum&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Observera att **Endast datum** funktionen tar hänsyn till serverns tidszon, inte operatorns.

### Geomarknadsföring

Geomarknadsföringsfunktionerna används för att ändra geografiska värden.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Avstånd</strong><br /> </td> 
   <td> Returnerar avståndet mellan två punkter som definieras av longitud och latitud, uttryckt i grader.<br /> </td> 
   <td> Distance(&lt;longitud A&gt;, &lt;latitud A&gt;, &lt;longitud B&gt;, &lt;latitud B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numeriskt

De numeriska funktionerna används för att konvertera text till tal.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Returnerar det absoluta värdet av ett tal<br /> </td> 
   <td> Abs(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Returnerar det lägsta heltalet som är större än eller lika med ett tal<br /> </td> 
   <td> Ceil(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Returnerar det största heltalet större än eller lika med ett tal<br /> </td> 
   <td> Floor(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Returnerar det största av två tal<br /> </td> 
   <td> Greatest(&lt;tal 1&gt;, &lt;tal 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Returnerar det minsta av två tal<br /> </td> 
   <td> Minst(&lt;tal 1&gt;, &lt;tal 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Returnerar resten av heltalsdivisionen av n1 med n2<br /> </td> 
   <td> Mod(&lt;tal 1&gt;, &lt;tal 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Procent</strong><br /> </td> 
   <td> Returnerar förhållandet mellan två tal uttryckta i procent<br /> </td> 
   <td> Procent(&lt;tal 1&gt;, &lt;tal 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Returnerar det slumpmässiga värdet<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Avrundar ett tal till n decimaler<br /> </td> 
   <td> Round(&lt;tal&gt;, &lt;antal decimaler&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Returnerar talets tecken<br /> </td> 
   <td> Sign(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Konverterar ett heltal till ett flyttal<br /> </td> 
   <td> ToDouble(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Konverterar ett flyttal till ett 64-bitars heltal<br /> </td> 
   <td> ToInt64(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Konverterar ett flyttal till ett heltal<br /> </td> 
   <td> ToInteger(&lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Trunkerar n1 till n2 decimaler<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Övriga

Tabellen innehåller de återstående funktionerna som är tillgängliga.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> Krypteringssträngen anges i argumentet<br /> </td> 
   <td> AESEncrypt()&lt;value&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Returnerar värdet 1 om villkoret är sant. Annars returneras värdet 2.<br /> </td> 
   <td> Case(When(&lt;villkor&gt;, &lt;värde 1&gt;), Else(&lt;värde 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Tar bort flaggan i värdet<br /> </td> 
   <td> ClearBit(&lt;identifierare&gt;, &lt;flagga&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Returnerar värde 2 om värde 1 är noll eller null, annars returneras värde 1<br /> </td> 
   <td> Coalesce(&lt;värde 1&gt;, &lt;värde 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Returnerar värde 3 om värde 1 = värde 2. Om inte returnerar värde 4.<br /> </td> 
   <td> Decode(&lt;värde 1&gt;, &lt;värde 2&gt;, &lt;värde 3&gt;, &lt;värde 4&gt;)<br /> </td>  
  </tr> 
  <!--<tr> 
   <td> <strong>DefaultFolder</strong><br /> </td> 
   <td> Returns value 3 if value 1 = value 2. If not returns value 4.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td>  
  </tr> -->
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Returnerar värde 1 (kan endast användas som en parameter för case-funktionen)<br /> </td> 
   <td> Else(&lt;value&gt;, &lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extraherar domänen från en e-postadress<br /> </td> 
   <td> GetEmailDomain(&lt;värde&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Hämtar URL:en för spegelsidservern<br /> </td> 
   <td> GetMirrorURL(&lt;värde&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Returnerar värdet 1 om uttrycket är true. Om inte returneras värde 2<br /> </td> 
   <td> Iif(&lt;villkor&gt;, &lt;värde 1&gt;, &lt;värde 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Anger om flaggan är i värdet<br /> </td> 
   <td> IsBitSet(&lt;identifierare&gt;, &lt;flagga&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Returnerar värde 2 om sträng 1 är tom, annars returneras värde 3<br /> </td> 
   <td> IsEmptyString()&lt;value&gt;, &lt;value&gt;, &lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUID</strong><br /> </td> 
   <td> Returnerar ett unikt ID<br /> </td> 
   <td> NewUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Returnerar den tomma strängen om argumentet är NULL<br /> </td> 
   <td> NoNull(&lt;värde&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Returnerar radnumret<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Tvingar flaggan i värdet<br /> </td> 
   <td> SetBit(&lt;identifierare&gt;, &lt;flagga&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Konverterar ett tal till ett booleskt värde<br /> </td> 
   <td> ToBoolean(&lt;tal&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Returnerar värdet 1 om uttrycket är true. Annars returneras värde 2 (kan bara användas som en parameter i case-funktionen)<br /> </td> 
   <td> When(&lt;tillstånd&gt;, &lt;värde 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Sträng

Strängfunktionerna används för att ändra en uppsättning strängar.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Anger om alla parametrar inte är null och inte tomma<br /> </td> 
   <td> AllNonNull2(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Anger om alla parametrar inte är null och inte tomma<br /> </td> 
   <td> AllNonNull3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Returnerar ASCII-värdet för det första tecknet i strängen.<br /> </td> 
   <td> Ascii()&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Returnerar tecknet som motsvarar ASCII-koden "n"<br /> </td> 
   <td> Char(&lt;number&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Returnerar positionen för sträng 2 i sträng 1.<br /> </td> 
   <td> Charindex(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> Returnerar strängens storlek i byte<br /> </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Returnerar den n:e raden (från 1 till n) i strängen<br /> </td> 
   <td> GetLine(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Returnerar den tredje parametern om de två första parametrarna är lika. Om inte returneras den sista parametern<br /> </td> 
   <td> IfEquals(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Anger om PM:et som skickas som en parameter är null<br /> </td> 
   <td> IsMemoNull()&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Sammanfogar de strängar som skickas som parametrar. Lägger till mellanrum mellan strängarna om det behövs.<br /> </td> 
   <td> JuxtWords(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Sammanfogar de strängar som skickas som parametrar. Lägger till mellanrum mellan strängarna om det behövs<br /> </td> 
   <td> JuxtWords3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Returnerar de första n tecknen i strängen<br /> </td> 
   <td> Left()&lt;string&gt;, &lt;number&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Returnerar strängens längd<br /> </td> 
   <td> Length(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Linje</strong><br /> </td> 
   <td> Extrahera rad n från sträng<br /> </td> 
   <td> Line(&lt;string&gt;,&lt;number&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Returnerar strängen i gemener<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Returnerar den slutförda strängen till vänster<br /> </td> 
   <td> LPad (&lt;string&gt;, &lt;number&gt;, &lt;char&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Tar bort blanksteg till vänster om strängen<br /> </td> 
   <td> Ltrim(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Returnerar en hexadecimal representation av MD5-nyckeln för en sträng<br /> </td> 
   <td> Md5Digest()&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>PMContains</strong><br /> </td> 
   <td> Anger om PM:et innehåller den sträng som skickas som en parameter<br /> </td> 
   <td> MemoContains(&lt;memo&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> Extraherar värdet för ett XML-fält från dess XPath och fältdata<br /> </td> 
   <td> NodeValue (&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Ersätter alla förekomster av ett angivet strängvärde med ett annat strängvärde.<br /> </td> 
   <td> Replace(&lt;string&gt;,&lt;string&gt;,&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Returnerar de sista n tecknen i strängen<br /> </td> 
   <td> Right(&lt;sträng&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Returnerar den slutförda strängen till höger<br /> </td> 
   <td> RPad(&lt;string&gt;, &lt;number&gt;, &lt;character&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Tar bort blanksteg till höger om strängen<br /> </td> 
   <td> Rtrim(&lt;sträng&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Hexadecimal representation av SHA256-nyckeln för en sträng.<br /> </td> 
   <td> Sha256Digest (&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Hexadecimal representation av SHA512-nyckeln för en sträng.<br /> </td> 
   <td> Sha512Digest (&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Returnerar strängen med den första bokstaven i varje ord med versaler<br /> </td> 
   <td> Smart(&lt;sträng&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extraherar delsträngen från tecken n1 i strängen och med längden n2<br /> </td> 
   <td> Substring(&lt;sträng&gt;, &lt;offset&gt;, &lt;längd&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Konverterar talet till en sträng<br /> </td> 
   <td> ToString()&lt;number&gt;, &lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Returnerar strängen med versaler<br /> </td> 
   <td> Upper(&lt;sträng&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Returnerar sekundärnyckeln för en länk som skickas som en parameter om de andra två parametrarna är lika<br /> </td> 
   <td> VirtualLink(&lt;tal&gt;, &lt;tal&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Returnerar sekundärnyckeln (text) för en länk som skickas som en parameter om de andra två parametrarna är lika<br /> </td> 
   <td> VirtualLinkStr(&lt;sträng&gt;, &lt;tal&gt;, &lt;tal&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Fönster

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Namn</strong><br /> </td> 
   <td> <strong>Beskrivning</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Över__</strong><br /> </td> 
   <td> Kör SQL-funktionsanropet som anges som första parameter, över partition eller Order By i de fält som anges som andra parameter<br /> </td> 
   <td> _Över_ (&lt;value&gt;, &lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Tillämpar en fallande sortering<br /> </td> 
   <td> Desc(&lt;värde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Sorterar resultatet i partitionen<br /> </td> 
   <td> OrderBy(&lt;värde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partitionerar resultatet av en fråga i en tabell<br /> </td> 
   <td> PartitionBy(&lt;värde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Genererar ett radnummer baserat på tabellpartitionen och en sorteringssekvens.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;värde 1&gt;), OrderBy(&lt;värde 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
