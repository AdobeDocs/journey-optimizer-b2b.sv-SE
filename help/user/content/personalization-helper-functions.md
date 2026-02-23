---
title: Hjälpfunktioner
description: Referenshandbok för hjälpfunktioner för personalisering i Journey Optimizer B2B edition. Den innehåller syntax och exempel för strängar, datum, matematik med mera.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: uttryck, redigerare, syntax, personalisering
exl-id: 04f78cdc-af2a-46ad-967d-2e129bd98e06
source-git-commit: 7a05e6aed76d15aa6d0d0a7dd244bf299d549782
workflow-type: tm+mt
source-wordcount: '4849'
ht-degree: 0%

---

# Hjälpfunktioner

Använd Helper-funktionerna i personaliseringsredigeraren för att definiera personaliserade innehållsupplevelser med precision och effektivitet genom att hantera data, utföra beräkningar och formatera innehåll. Utforska och experimentera med dessa funktioner, operatorer och hjälpredor för att ta reda på hur de samarbetar för att hjälpa er att skapa skräddarsydda, datadrivna resor.

>[!AVAILABILITY]
>
>Hjälpfunktioner är tillgängliga för [!DNL Journey Optimizer B2B Edition]-miljöer som har etablerats på den [förenklade arkitekturen](../simplified-architecture.md).

## Sammanställningsfunktioner

Använd aggregeringsfunktioner för att gruppera flera värden för att skapa ett enda sammanfattningsvärde. Du kan också använda array- och listfunktioner för att definiera interaktioner med arrayer, listor och strängar enklare.

### medel {#average}

Använd funktionen `average` för att returnera det aritmetiska medelvärdet för alla markerade värden i arrayen.

+++Syntax

```sql
{%= average(array) %}
```

**Exempel**

Följande åtgärd returnerar genomsnittspriset för alla order.

```sql
{%=average(orders.order.price)%}
```

+++

### antal {#count}

Använd funktionen `count` för att returnera antalet element i den angivna arrayen.

+++Syntax

```sql
{%= count(array) %}
```

**Exempel**

Följande åtgärd returnerar antalet order i arrayen.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Använd funktionen `max` för att returnera det största av alla markerade värden i arrayen.

+++Syntax

```sql
{%= max(array) %}
```

**Exempel**

Följande åtgärd returnerar det högsta priset för alla order.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Använd funktionen `min` för att returnera det minsta av alla markerade värden i arrayen.

+++Syntax

```sql
{%= min(array) %}
```

**Exempel**

Följande åtgärd returnerar det lägsta priset för alla order.

```sql
{%=min(orders.order.price) %}
```

+++

### summa {#sum}

Använd funktionen `sum` för att returnera summan av alla markerade värden i arrayen.

+++Syntax

```sql
{%= sum(array) %}
```

**Exempel**

Följande operation returnerar summan av alla orderpriser.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Aritmetiska funktioner {#maths}

Använd aritmetiska funktioner för att utföra grundläggande beräkningar på värden.

### lägg till {#add}

Använd funktionen `+` (addition) för att hitta summan av två argumentuttryck.

+++Syntax

```sql
{%= double + double %}
```

**Exempel**

Följande operation summerar priset på två olika produkter.

```sql
{%= product1.price + product2.price %}
```

+++

### multiplicera {#multiply}

Använd funktionen `*` (multiplikation) för att hitta produkten av två argumentuttryck.

+++Syntax

```sql
{%= double * double %}
```

**Exempel**

Följande åtgärd hittar produkten i lagret och priset på en produkt för att hitta produktens bruttovärde.

```sql
{%= product.inventory * product.price %}
```

+++

### ta bort {#substract}

Använd funktionen `-` (subtraktion) för att hitta skillnaden mellan två argumentuttryck.

+++Syntax

```sql
{%= double - double %}
```

**Exempel**

Följande åtgärd identifierar prisskillnaden mellan två olika produkter.

```sql
{%= product1.price - product2.price %}
```

+++

### dividera {#divide}

Använd funktionen `/` (division) för att hitta kvoten mellan två argumentuttryck.

+++Syntax

```sql
{%= double / double %}
```

**Exempel**

I följande åtgärd hittas kvoten mellan de totala sålda produkterna och de totala intjänade pengarna för att se den genomsnittliga kostnaden per artikel.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### rest {#remainder}

Använd funktionen `%` (rest) för att hitta resten efter att de två argumentuttrycken har delats.

+++Syntax

```sql
{%= double % double %}
```

**Exempel**

Följande åtgärd kontrollerar om personens ålder är delbar med fem.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Arrayer och listfunktioner {#arrays}

Använd de här funktionerna för att underlätta interaktionen med arrayer, listor och strängar.

### countOnlyNull {#count-only-null}

Använd funktionen `countOnlyNull` för att räkna antalet null-värden i en lista.

+++Syntax

```sql
{%= countOnlyNull(array) %}
```

**Exempel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Returnerar 3.

+++

### countWithNull {#count-with-null}

Använd funktionen `countWithNull` för att räkna alla element i en lista inklusive null-värden.

+++Syntax

```sql
{%= countWithNull(array) %}
```

**Exempel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Returnerar 6.

+++

### distinkt {#distinct}

Använd funktionen `distinct` för att hämta värden från en array eller lista där dubblettvärden har tagits bort.

+++Syntax

```sql
{%= distinct(array) %}
```

**Exempel**

Följande åtgärd anger personer som har gjort beställningar i mer än en butik.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### clearCountWithNull {#distinct-count-with-null}

Använd funktionen `distinctCountWithNull` för att räkna antalet olika värden i en lista inklusive null-värden.

+++Syntax

```sql
{%= distinctCountWithNull(array) %}
```

**Exempel**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Returnerar 3.

+++

### head {#head}

Använd funktionen `head` för att returnera det första objektet i en array eller lista.

+++Syntax

```sql
{%= head(array) %}
```

**Exempel**

Följande åtgärd returnerar den första av de fem främsta beställningarna med det högsta priset. Mer information om funktionen `topN` finns i avsnittet [first `n` i array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

Funktionen `topN` sorterar en array i fallande ordning baserat på det angivna numeriska uttrycket och returnerar de första `N` objekten. Om arraystorleken är mindre än `N` returneras hela den sorterade arrayen.

+++Syntax

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{ARRAY}` | Arrayen eller listan som ska sorteras. |
| `{VALUE}` | Den egenskap som används för att sortera arrayen eller listan. |
| `{AMOUNT}` | Antalet artiklar som ska returneras. |

**Exempel**

Följande åtgärd returnerar de första fem beställningarna med det lägsta priset.

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

Använd funktionen `in` för att avgöra om ett objekt är medlem i en array eller lista.

+++Syntax

```sql
{%= in(value, array) %}
```

**Exempel**

Följande åtgärd definierar personer med födelsedagar i mars, juni eller september.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### inkluderar {#includes}

Använd funktionen `includes` för att avgöra om en array eller lista innehåller ett visst objekt.

+++Syntax

```sql
{%= includes(array,item) %}
```

**Exempel**

Följande åtgärd definierar personer vars favoritfärg innehåller rött.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### korsar {#intersects}

Funktionen `intersects` används för att avgöra om två arrayer eller listor har minst en gemensam medlem.

+++Syntax

```sql
{%= intersects(array1, array2) %}
```

**Exempel**

Följande åtgärd definierar personer vars favoritfärger innehåller minst en röd, blå eller grön färg.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

Funktionen `bottomN` sorterar en array i stigande ordning baserat på det angivna numeriska uttrycket och returnerar de första `N` objekten. Om arraystorleken är mindre än `N` returneras hela den sorterade arrayen.

+++Syntax

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beskrivning |
| --------- | ----------- | 
| `{ARRAY}` | Arrayen eller listan som ska sorteras. |
| `{VALUE}` | Den egenskap som används för att sortera arrayen eller listan. |
| `{AMOUNT}` | Antalet artiklar som ska returneras. |

**Exempel**

Följande åtgärd returnerar de fem sista beställningarna med det högsta priset.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Använd funktionen `notIn` för att avgöra om ett objekt inte är medlem i en array eller lista.

>[!NOTE]
>
>`notIn`-funktionen *ser också* till att inget av värdena är lika med null. Resultatet är därför inte en exakt negation av funktionen `in`.

+++Syntax

```sql
{%= notIn(value, array) %}
```

**Exempel**

Följande åtgärd definierar personer med födelsedagar som inte är i mars, juni eller september.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Använd funktionen `subsetOf` för att avgöra om en viss array (array A) är en delmängd av en annan array (array B). Det vill säga att alla element i array A är element i array B.

+++Syntax

```sql
{%= subsetOf(array1, array2) %}
```

**Exempel**

Följande åtgärd definierar personer som har besökt alla sina favoritstäder.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### supersetOf {#superset}

Använd funktionen `supersetOf` för att avgöra om en viss array (array A) är en överordnad mängd till en annan array (array B). Arrayen A innehåller alltså alla element i array B.

+++Syntax

```sql
{%= supersetOf(array1, array2) %}
```

**Exempel**

Följande åtgärd definierar personer som har ätit sushi och pizza minst en gång.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Datum- och tidsfunktioner {#date-time}

Använd datum- och tidsfunktionerna för att utföra datum- och tidsåtgärder på värden.

### addDays {#add-days}

Funktionen `addDays` justerar ett givet datum med ett angivet antal dagar och använder positiva värden för att öka och negativa värden för minskning.

+++Syntax

```sql
{%= addDays(date, number) %}
```

**Exempel**

* Indata: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Utdata: `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

Funktionen `addHours` justerar ett givet datum med ett angivet antal timmar, och använder positiva värden för att öka och negativa värden för minskning.

+++Syntax

```sql
{%= addHours(date, number) %}
```

**Exempel**

* Indata: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Utdata: `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

Funktionen `addMinutes` justerar ett givet datum med ett angivet antal minuter och använder positiva värden för att öka och negativa värden för minskning.

+++Syntax

```sql
{%= addMinutes(date, number) %}
```

**Exempel**

* Indata: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Utdata: `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

Funktionen `addMonths` justerar ett givet datum med ett angivet antal månader och använder positiva värden för att öka och negativa värden för minskning.

+++Syntax

```sql
{%= addMonths(date, number) %}
```

**Exempel**

* Indata: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Utdata: `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

Funktionen `addSeconds` justerar ett givet datum med ett angivet antal sekunder och använder positiva värden för att öka och negativa värden för minskning.

+++Syntax

```sql
{%= addSeconds(date, number) %}
```

**Exempel**

* Indata: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Utdata: `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

Funktionen `addYears` justerar ett givet datum med ett angivet antal år och använder positiva värden för att öka och negativa värden för minskning.

+++Syntax

```sql
{%= addYears(date, number) %}
```

**Exempel**

* Indata: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Utdata: `2026-11-01T17:19:51Z`

+++

### age {#age}

Använd funktionen `age` för att hämta åldern från ett visst datum.

+++Syntax

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

Funktionen `ageInDays` beräknar antalet dagar som förflutit mellan det angivna datumet och det aktuella datumet. Negativ används för framtida datum och positiv för tidigare datum.

+++Syntax

```sql
{%= ageInDays(date) %}
```

**Exempel**

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asien/Kolkata)

* Indata: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Utdata: `5`

+++

### ageInMonths {#age-months}

Funktionen `ageInMonths` beräknar antalet månader som förflutit mellan det angivna datumet och det aktuella datumet. Negativ används för framtida datum och positiv för tidigare datum.

+++Syntax

```sql
{%= ageInMonths(date) %}
```

**Exempel**

currentDate = 2025-01-07T12:22:46.993748+05:30(Asia/Kolkata)

* Indata: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Utdata: `12`

+++

### compareDates {#compare-dates}

Funktionen `compareDates` jämför det första indatadatumet med det andra. Returnerar 0 om date1 är lika med date2, -1 om date1 kommer före date2 och 1 om date1 kommer efter date2.

+++Syntax

```sql
{%= compareDates(date1, date2) %}
```

**Exempel**

* Indata: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Utdata: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

Funktionen `convertZonedDateTime` konverterar ett datum/tid till en given tidszon.

+++Syntax

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Exempel**

* Indata: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Utdata: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Använd funktionen `currentTimeInMillis` för att hämta aktuell tid i epok i millisekunder.

+++Syntax

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

Använd funktionen `dateDiff` för att hämta skillnaden mellan två datum i antal dagar.

+++Syntax

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

`dayOfMonth` returnerar talet som representerar dagen i månaden.

+++Syntax

```sql
{%= dayOfMonth(datetime) %}
```

**Exempel**

* Indata: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Utdata: `5`

+++

### DayOfWeek {#day-week}

Använd funktionen `dayOfWeek` för att hämta veckodagen.

+++Syntax

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Använd funktionen `dayOfYear` för att hämta dagen på året.

+++Syntax

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

Funktionen `diffInSeconds` returnerar skillnaden mellan två datum i sekunder.

+++Syntax

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Exempel**

* Indata: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Utdata: `50`

+++

### extractHours {#extract-hours}

Funktionen `extractHours` extraherar timkomponenten från en given tidsstämpel.

+++Syntax

```sql
{%= extractHours(date) %}
```

**Exempel**

* Indata: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Utdata: `17`

+++

### extractMinutes {#extract-minutes}

Funktionen `extractMinutes` extraherar minutkomponenten från en given tidsstämpel.

+++Syntax

```sql
{%= extractMinutes(date) %}
```

**Exempel**

* Indata: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Utdata: `19`

+++

### extractMonths {#extract-months}

Funktionen `extractMonth` extraherar månadskomponenten från en viss tidsstämpel.

+++Syntax

```sql
{%= extractMonths(date) %}
```

**Exempel**

* Indata: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Utdata: `11`

+++

### extractSeconds {#extract-seconds}

Funktionen `extractSeconds` extraherar den andra komponenten från en viss tidsstämpel.

+++Syntax

```sql
{%= extractSeconds(date) %}
```

**Exempel**

* Indata: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Utdata: `51`

+++

### formatDate {#format-date}

Använd funktionen `formatDate` för att formatera ett datum- och tidvärde. Formatet måste vara ett giltigt Java `DateTimeFormat`-mönster.

+++Syntax

```sql
{%= formatDate(datetime, format) %}
```

Där den första strängen är datumattributet och det andra värdet är hur du vill att datumet ska konverteras och visas.

>[!NOTE]
>
> Om ett datummönster är ogiltigt återgår datumet till ISO-standardformatet.
>
> Du kan använda Java-datumformateringsfunktioner som sammanfattas i [Oracle-dokumentationen](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exempel**

Följande åtgärd returnerar datumet i följande format: MM/DD/YY.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Mönstertecken {#pattern-characters}

Vissa mönsterbokstäver kan se likadana ut, men representerar olika koncept.

| Mönster | Betydelse | Exempel (för `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Kalenderår (standardår) | `2023` |
| `Y` | Veckobaserat år (ISO 8601). Den kan skilja sig åt vid årsgränser. | `2024` (31 december 2023 infaller under den första veckan 2024) |
| `M` | Månad på året (1-12 eller text som `Jan`, `January`) | `12` eller `Dec` |
| `m` | Timme (0-59) | `15` |
| `d` | Månadsdag (1-31) | `31` |
| `D` | Årsdag (1-366) | `365` |

#### Formatera datum med språkstöd {#format-date-locale}

Du kan använda funktionen `formatDate` för att formatera ett datum- och tidvärde till motsvarande språkkänsliga representation, till exempel för önskad språkinställning. Formatet måste vara ett giltigt Java `DateTimeFormat`-mönster.

+++Syntax

```sql
{%= formatDate(datetime, format, locale) %}
```

Där den första strängen är datumattributet är det andra värdet hur du vill att datumet ska konverteras och visas, och det tredje värdet representerar språkområdet i strängformat.

>[!NOTE]
>
> Om ett datummönster är ogiltigt återgår datumet till ISO-standardformatet.
>
> Du kan använda Java-datumformateringsfunktioner enligt sammanfattningen i [Oracle-dokumentationen](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Du kan använda formatering och giltiga språkinställningar enligt sammanfattningen i [Oracle-dokumentationen](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) och [Språkinställningar som stöds](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Exempel**

Följande åtgärd returnerar datumet i följande format: MM/dd/YY och språkområde FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

Funktionen `getCurrentZonedDateTime` returnerar aktuellt datum och aktuell tid med tidszonsinformation.

+++Syntax

```sql
{%= getCurrentZonedDateTime() %}
```

**Exempel**

* Indata: `{%= getCurrentZonedDateTime() %}`
* Utdata: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

Funktionen `diffInHours` returnerar skillnaden mellan två datum i timmar.

+++Syntax

```sql
{%= diffInHours(endDate, startDate) %}
```

**Exempel**

* Indata: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Utdata: `10`

+++

### diffInMinutes {#diff-minutes}

Funktionen `diffInMinutes` returnerar skillnaden mellan två datum i minuter.

+++Syntax

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Exempel**

* Indata: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Utdata: `60`

+++

### diffInMonths {#months-difference}

Funktionen `diffInMonths` returnerar skillnaden mellan två datum i månader.

+++Syntax

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Exempel**

* Indata: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Utdata: `3`

+++

### setDays {#set-days}

Använd funktionen `setDays` för att ange dag i månaden för angivet datum/tid.

+++Syntax

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Använd funktionen `setHours` för att ange timmen för datum/tid.

+++Syntax

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

Funktionen `toDateTime` konverterar sträng till datum. Det returnerar epokdatumet som utdata för ogiltiga indata.

+++Syntax

```sql
{%= toDateTime(string, string) %}
```

**Exempel**

* Indata: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Utdata: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Använd funktionen `toUTC` för att konvertera en datetime till UTC.

+++Syntax

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Använd funktionen `truncateToStartOfDay` om du vill ändra ett givet datum/tid genom att ställa in det till början av dagen med tiden vid 0:00.

+++Syntax

```sql
{%= truncateToStartOfDay(date) %}
```

**Exempel**

* Indata: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Utdata: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Använd funktionen `truncateToStartOfQuarter` som används för att korta av ett datum-tid till den första dagen i kvarteret (till exempel 1 januari, 1 april, 1 juli och 1 oktober) klockan 00:00.

+++Syntax

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Exempel**

* Indata: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Utdata: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

Funktionen `truncateToStartOfWeek` ändrar ett visst datum/tid genom att ställa in det till veckans början (måndag 0:00).

+++Syntax

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Exempel**

* Indata: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Utdata: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Använd funktionen `truncateToStartOfYear` för att ändra ett visst datum/tid genom att trunkera det till årets första dag (1 januari) kl. 00:00.

+++Syntax

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Exempel**

* Indata: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Utdata: `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Använd funktionen `weekOfYear` för att hämta årets vecka.

+++Syntax

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

Använd funktionen `diffInYears` för att returnera skillnaden mellan två datum i termer av år.

+++Syntax

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Exempel**

* Indata: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Utdata: `5`

+++

## Operatörsfunktioner {#operators}

Använd de booleska funktionerna och jämförelsefunktionerna för att utföra logiska utvärderingar.

### och {#and}

Funktionen `and` används för att skapa en logisk koppling.

+++Syntax

```sql
{%= query1 and query2 %}
```

**Exempel**

Följande operation returnerar alla personer med hemland (Frankrike) och födelseår (1985).

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### eller {#or}

Funktionen `or` används för att skapa en logisk förskjutning.

+++Syntax

```sql
{%= query1 or query2 %}
```

**Exempel**

Följande operation returnerar alla personer med hemland (Frankrike) eller födelseår (1985).

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### är lika med {#operator-equals}

Funktionen `=` (lika med) kontrollerar om ett värde eller uttryck är lika med ett annat värde eller uttryck.

+++Syntax

```sql
{%= expression = value %}
```

**Exempel**

Följande åtgärd kontrollerar om hemadresslandet är Frankrike.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### inte lika med {#notequal}

Funktionen `!=` (inte lika med) kontrollerar om ett värde eller uttryck är **inte** lika med ett annat värde eller uttryck.

+++Syntax

```sql
{%= expression != value %}
```

**Exempel**

Följande åtgärd kontrollerar om hemadresslandet inte är Frankrike.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### större än {#greaterthan}

Använd funktionen `>` (större än) för att kontrollera om det första värdet är större än det andra värdet.

+++Syntax

```sql
{%= expression1 > expression2 %}
```

**Exempel**

Följande operation definierar personer som är födda strikt efter 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### större än eller lika med {#greaterthanorequal}

Använd funktionen `>=` (större än eller lika med) för att kontrollera om det första värdet är större än eller lika med det andra värdet.

+++Syntax

```sql
{%= expression1 >= expression2 %}
```

**Exempel**

Följande operation definierar personer födda i eller efter 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### mindre än {#lessthan}

Använd jämförelsefunktionen `<` (mindre än) för att kontrollera om det första värdet är mindre än det andra värdet.

+++Syntax

```sql
{%= expression1 < expression2 %}
```

**Exempel**

Följande åtgärd definierar personer som är födda före 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### mindre än eller lika med{#lessthanorequal}

Använd jämförelsefunktionen `<=` (mindre än eller lika med) för att kontrollera om det första värdet är mindre än eller lika med det andra värdet.

+++Syntax

```sql
{%= expression1 <= expression2 %}
```

**Exempel**

Följande operation definierar personer födda år 2000 eller tidigare.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Dynamiska funktioner {#dynamic-helpers}

Använd de dynamiska hjälpfunktionerna för att använda villkorsstyrda utvärderingar, upprepningar och variabeltilldelningar för dynamisk personalisering.

### Standardvärde för reserv {#default-value}

Hjälpprogrammet `Default Fallback Value` används för att returnera ett standardreservvärde om ett attribut är tomt eller null. Den här mekanismen fungerar för profilattribut och resthändelser.

+++Syntax

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

I det här exemplet visas värdet `there` om attributet `firstName` för den här profilen är tomt eller null.

+++

### if (conditions) {#if-function}

Hjälpprogrammet `if` används för att definiera ett villkorsblock.
Om uttrycksutvärderingen returnerar true återges blocket, i annat fall hoppas det över.

+++Syntax

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Efter hjälpen för `if` kan du ange en `else`-sats för att ange ett kodblock som ska köras, om samma villkor är falskt.
Programsatsen `elseif` anger ett nytt villkor som ska testas om den första programsatsen returnerar false.


**Format**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### såvida inte {#unless}

Använd hjälpen för `unless` för att definiera ett villkorsstyrt block. Om uttrycksutvärderingen returnerar false återges blocket som motsatt `if`-hjälpen.

+++Syntax

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exempel**

Återge visst innehåll baserat på e-postadresstillägget:

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### var {#each}

Använd hjälpen för `each` för att iterera över en array.

Hjälpstrukturen är ```{{#each ArrayName}}``` Ditt innehåll `{{/each}}`

Du kan använda nyckelordet `this` i blocket för att referera till de enskilda arrayobjekten. Använd `{{@index}}` för att återge indexvärdet för arrayens element.

+++Syntax

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Exempel**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Exempel**

Visa en lista över produkter som den här användaren har i kundvagnen:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### med {#with}

Använd hjälpen för `with` för att ändra utvärderingstoken för malldel.

+++Syntax

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Hjälpprogrammet `with` är också användbart för att definiera en genvägsvariabel.

**Exempel**

Använd `with` för att skapa alias för långa variabelnamn för kortare:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### let {#let}

Funktionen `let` tillåter att ett uttryck lagras som en variabel som kan användas senare i en fråga.

+++Syntax

```sql
{% let variable = expression %} {{variable}}
```

**Exempel**

I följande exempel kan du beräkna den totala summan av priserna för produkter i vagnen med priser mellan 100 och 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Körningsmetadata {#execution-metadata}

>[!AVAILABILITY]
>
>Den här funktionen är begränsad. Kontakta din Adobe-representant för att få åtkomst.

Använd `executionMetadata` för att hämta och lagra anpassade nyckelvärdepar dynamiskt i meddelandekörningskontexten.

Med den här funktionen kan ni lägga till sammanhangsbaserad information till alla inbyggda åtgärder från era kampanjer eller resor. Använd det för att exportera sammanhangsbaserade data i realtid till externa system för olika syften, t.ex. spårning, analys, personalisering och nedladdning.

>[!NOTE]
>
>Anpassade åtgärder stöder inte funktionen `executionMetadata`.

Du kan till exempel använda hjälpen för `executionMetadata` för att lägga till ett specifikt ID för varje leverans som skickas till varje profil. Den här informationen genereras under körningen och de inbyggda körningsmetadata som sedan kan exporteras för avstämning i efterföljande led med en extern rapporteringsplattform.

+++Syntax

```
{{executionMetadata key="your_key" value="your_value"}}
```

I den här syntaxen refererar `key` till metadatanamnet och `value` är de metadata som ska bevaras.

**Så här fungerar det**

Välj ett element från ditt kanalinnehåll i en kampanj eller resa och lägg till `executionMetadata`-hjälpen i det här elementet med hjälp av anpassningsredigeraren.

>[!NOTE]
>
>Funktionen `executionMetadata` visas inte när själva innehållet visas.

Vid körning läggs metadatavärdet till i den befintliga **[!UICONTROL Message Feedback Event Dataset]** med följande schemaläggning:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Det finns en övre gräns på 2 kB för nyckelvärdepar per åtgärd. Om gränsen på 2 kB överskrids levereras meddelandet fortfarande, men något av nyckelvärdeparen kan trunkeras.

**Exempel**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

I det här exemplet är den resulterande entiteten `profile.person.name.firstName` = &quot;Alex&quot;:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Kartfunktioner {#maps}

Använd kartfunktioner i personalisering för att underlätta interaktionen med kartor.

### get {#get}

Använd funktionen `get` för att hämta värdet för en karta för en given nyckel.

+++Syntax

```sql
{%= get(map, string) %}
```

**Exempel**

Följande åtgärd hämtar värdet för identitetskartan för nyckeln `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### tangenter {#keys}

Använd funktionen `keys` för att hämta alla nycklar för en given karta.

+++Syntax

```sql
{%= keys(map) %}
```

**Exempel**

Följande åtgärd hämtar alla nycklar för kartan `identityMap`.

```sql
{%= keys(identityMap) %}
```

+++

### values {#values}

Funktionen `values` används för att hämta alla värden för en given karta.

+++Syntax

```sql
{%= values(map) %}
```

**Exempel**

Följande åtgärd hämtar alla värden för kartan `identityMap`.

```sql
{%= values(identityMap) %}
```

+++

## Matematiska funktioner {#math}

Lär dig använda Math-funktioner i personaliseringsredigeraren.

### absolut {#absolute}

Använd funktionen `absolute` för att konvertera ett tal till dess absoluta värde.

+++Syntax

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Använd funktionen `formatNumber` om du vill formatera ett tal i dess språkkänsliga representation.

Den accepterar ett tal och en sträng som representerar språkområdet och returnerar en formaterad sträng med talet i det önskade språkområdet.

+++Syntax

```sql
{%= formatNumber(number/double,string) %}: string
```

Du kan använda formatering och giltiga språkinställningar enligt en sammanfattning i [Oracle-dokumentationen](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) och [Språkinställningar som stöds](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Exempel**

Den här frågan returnerar en formaterad sträng på arabiska som motsvarar 123456.789 som indatanummer.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

Använd funktionen `random` för att returnera ett slumpmässigt värde mellan 0 och 1.

+++Syntax

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

Använd funktionen `roundDown` för att avrunda ett tal nedåt.

+++Syntax

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

Använd funktionen `roundUp` för att avrunda ett tal uppåt.

+++Syntax

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

Funktionen `toHexString` konverterar alla tal till sin hexadecimala sträng.

+++Syntax

```sql
{%= toHexString(number) %}: string
```

**Exempel**

Den här frågan returnerar det hexadecimala värdet 158 som 9e.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Använd funktionen `toInt` för att konvertera typer (tal, double, integer, long, float, short, byte, boolean, string) till ett heltal.

+++Syntax

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Exempel**

Den här frågan returnerar heltalsvärdet 42,6 som 42.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Använd funktionen `toPercentage` för att konvertera ett tal till procent.

+++Syntax

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Använd funktionen `toPrecision` för att konvertera ett tal till den precision som krävs.

+++Syntax

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

Funktionen `toString` konverterar alla tal till sin strängbeteckning.

+++Syntax

```sql
{%= toString(string) %}: string
```

**Exempel**

Frågan returnerar `"12"`.

```sql
{%= toString(12) %} 
```

+++

## Objektfunktioner {#objects}

Objektfunktioner för att fråga efter objektegenskaper eller attribut.

### isNull {#isNull}

Funktionen `isNull` avgör om en objektreferens inte finns.

+++Syntax

```sql
{%= isNull(object) %}
```

**Exempel**

Följande åtgärd kontrollerar om personens hemadress inte finns.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

Funktionen `isNotNull` avgör om det finns en objektreferens.

+++Syntax

```sql
{%= isNotNull(object) %}
```

**Exempel**

Följande åtgärd kontrollerar om personens hemadress finns.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Strängfunktioner {#string-functions}

Lär dig hur du använder strängfunktioner i personaliseringsredigeraren.

### camelCase {#camelCase}

Funktionen `camelCase` ändrar den första bokstaven i varje ord i en sträng till versal.

+++Syntax

```sql
{%= camelCase(string)%}
```

**Exempel**

Följande funktion ändrar den första bokstaven i ett ord till versal i profilens gatuadress.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

Funktionen `charCodeAt` returnerar ASCII-värdet för ett tecken, precis som funktionen `charCodeAt` i JavaScript. Den tar en sträng och ett heltal (som definierar positionen för ett tecken) som indataargument och returnerar motsvarande ASCII-värde.

+++Syntax

```sql
{%= charCodeAt(string,int) %}: int
```

**Exempel**

Följande funktion returnerar ASCII-värdet `o` (111).

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

Funktionen `concat` kombinerar två strängar till en.

+++Syntax

```sql
{%= concat(string,string) %}
```

**Exempel**

Följande funktion kombinerar profilens ort och land i en enda sträng.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### innehåller {#contains}

Använd funktionen `contains` för att avgöra om en sträng innehåller en angiven delsträng.

+++Syntax

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `STRING_1` | Strängen som kontrollen ska utföras på. |
| `STRING_2` | Den sträng som ska sökas efter i den första strängen. |
| `CASE_SENSITIVE` | En valfri parameter som avgör om kontrollen är skiftlägeskänslig. Möjliga värden: true (standard) / false. |

**Exempel**

* Följande funktion kontrollerar om profilens förnamn innehåller bokstaven A (i versaler eller gemener). Om profilen gör det returnerar den `true`. Annars returneras `false`.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* Följande fråga avgör, med skiftlägeskänslighet, om personens e-postadress innehåller strängen `2010@gm`.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

Använd funktionen `doesNotContain` för att avgöra om en sträng inte innehåller en angiven delsträng.

+++Syntax

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `STRING_1` | Strängen som kontrollen ska utföras på. |
| `STRING_2` | Den sträng som ska sökas efter i den första strängen. |
| `CASE_SENSITIVE` | En valfri parameter som avgör om kontrollen är skiftlägeskänslig. Möjliga värden: true (standard) / false. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens e-postadress inte innehåller strängen `2010@gm`.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

Använd funktionen `doesNotEndWith` för att avgöra om en sträng inte avslutas med en angiven delsträng.

+++Syntax

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Den sträng som ska sökas efter i den första strängen. |
| `{CASE_SENSITIVE}` | En valfri parameter som avgör om kontrollen är skiftlägeskänslig. Möjliga värden: true (standard) / false. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens e-postadress inte avslutas med `.com`.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

Använd funktionen `doesNotStartWith` för att avgöra om en sträng inte börjar med en angiven delsträng.

+++Syntax

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Den sträng som ska sökas efter i den första strängen. |
| `{CASE_SENSITIVE}` | En valfri parameter som avgör om kontrollen är skiftlägeskänslig. Möjliga värden: true (standard) / false. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens namn inte börjar med `Joe`.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

Använd funktionen `encode64` om du vill koda en sträng för att bevara personlig information (PI), till exempel som ska inkluderas i en URL.

+++Syntax

```sql
{%= encode64(string) %}
```

+++

### endsWith {#endsWith}

Använd funktionen `endsWith` för att avgöra om en sträng avslutas med en angiven delsträng.

+++Syntax

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Den sträng som ska sökas efter i den första strängen. |
| `{CASE_SENSITIVE}` | En valfri parameter som avgör om kontrollen är skiftlägeskänslig. Möjliga värden: true (standard) / false. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens e-postadress slutar med `.com`.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### är lika med {#equals}

Använd funktionen `equals` för att avgöra om en sträng är lika med den angivna strängen, med skiftlägeskänslighet.

+++Syntax

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Strängen som ska jämföras med den första strängen. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens namn är `John`.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

Använd funktionen `equalsIgnoreCase` för att avgöra om en sträng är lika med den angivna strängen, utan skiftlägeskänslighet.

+++Syntax

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Strängen som ska jämföras med den första strängen. |

**Exempel**

Följande fråga avgör, utan skiftlägeskänslighet, om personens namn är `John`.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Använd funktionen `extractEmailDomain` för att extrahera domänen för en e-postadress.

+++Syntax

```sql
{%= extractEmailDomain(string) %}
```

**Exempel**

Följande fråga extraherar e-postdomänen för den personliga e-postadressen.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Använd funktionen `formatCurrency` om du vill konvertera ett tal till motsvarande språkkänsliga valutarepresentation beroende på vilket språk som skickas som en sträng i det andra argumentet.

+++Syntax

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Exempel**

Frågan returnerar 56,00 GBP

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Använd funktionen `getUrlHost` för att hämta värdnamnet för en URL.

+++Syntax

```sql
{%= getUrlHost(string) %}: string
```

**Exempel**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Returnerar &quot;www.myurl.com&quot;

+++

### getUrlPath {#get-url-path}

Använd funktionen `getUrlPath` för att hämta sökvägen efter domännamnet för en URL.

+++Syntax

```sql
{%= getUrlPath(string) %}: string
```

**Exempel**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Returnerar &quot;/contact.html&quot;

+++

### getUrlProtocol {#get-url-protocol}

Använd funktionen `getUrlProtocol` för att hämta protokollet för en URL.

+++Syntax

```sql
{%= getUrlProtocol(string) %}: string
```

**Exempel**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Returnerar &quot;http&quot;

+++

### indexOf {#index-of}

Använd funktionen `indexOf` för att returnera positionen (i det första argumentet) för den första förekomsten av den andra parametern. Returnerar -1 om det inte finns någon matchning.

+++Syntax

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Strängen som ska sökas i den första parametern |

**Exempel**

```sql
{%= indexOf("hello world","world" ) %}
```

Returnerar 6.

+++

### isEmpty {#isEmpty}

Använd funktionen `isEmpty` för att avgöra om en sträng är tom.

+++Syntax

```sql
{%= isEmpty(string) %}
```

**Exempel**

Följande funktion returnerar &#39;true&#39; om profilens mobiltelefonnummer är tomt. Annars returneras `false`.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Använd funktionen `isNotEmpty` för att avgöra om en sträng inte är tom.

+++Syntax

```sql
{= isNotEmpty(string) %}: boolean
```

**Exempel**

Följande funktion returnerar &#39;true&#39; om profilens mobiltelefonnummer inte är tomt. Annars returneras `false`.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Använd funktionen `lastIndexOf` för att returnera positionen (i det första argumentet) för den sista förekomsten av den andra parametern. Returnerar -1 om det inte finns någon matchning.

+++Syntax

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Strängen som ska sökas i den första parametern |

**Exempel**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Returnerar 7.

+++

### leftTrim {#leftTrim}

Använd funktionen `leftTrim` för att ta bort blanksteg från början av en sträng.

+++Syntax

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Använd funktionen `length` för att hämta antalet tecken i en sträng eller ett uttryck.

+++Syntax

```sql
{%= length(string) %}
```

**Exempel**

Följande funktion returnerar längden på profilens stadsnamn.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### gilla {#like}

Använd funktionen `like` för att avgöra om en sträng matchar ett angivet mönster.

+++Syntax

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Det uttryck som ska matchas mot den första strängen. Det finns två specialtecken som stöds för att skapa ett uttryck: `%` och `_`. <ul><li>`%` används för att representera noll eller flera tecken.</li><li>`_` används för att representera exakt ett tecken.</li></ul> |

**Exempel**

Följande fråga hämtar alla städer där profiler som innehåller mönstret `es` finns.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

Använd funktionen `lowerCase` för att konvertera en sträng till gemena bokstäver.

+++Syntax

```sql
{%= lowerCase(string) %}
```

**Exempel**

Den här funktionen konverterar profilens förnamn till gemener.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matchar {#matches}

Använd funktionen `matches` för att avgöra om en sträng matchar ett visst reguljärt uttryck. Mer information om att matcha mönster i reguljära uttryck finns i [Oracle-dokumentationen](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Syntax

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exempel**

Följande fråga avgör, utan skiftlägeskänslighet, om personens namn börjar med `John`.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### mask {#mask}

Använd funktionen `mask` om du vill ersätta en del av en sträng med X-tecken.

+++Syntax

```sql
{%= mask(string,integer,integer) %}
```

**Exempel**

Följande fråga ersätter strängen &quot;123456789&quot; med &quot;X&quot;-tecken, med undantag för de första och de sista två tecknen.

```sql
{%= mask("123456789",1,2) %}
```

Frågan returnerar `1XXXXXX89`.

+++

### md5 {#md5}

Använd funktionen `md5` för att beräkna och returnera md5-hash för en sträng.

+++Syntax

```sql
{%= md5(string) %}: string
```

**Exempel**

```sql
{%= md5("hello world") %}
```

Returnerar &quot;5eb63bbbe01eed093cb22bb8f5acdc3&quot;

+++

### notEqualTo {#notEqualTo}

Använd funktionen `notEqualTo` för att avgöra om en sträng inte är lika med den angivna strängen.

+++Syntax

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Strängen som ska jämföras med den första strängen. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens namn inte är `John`.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Använd funktionen `notEqualWithIgnoreCase` för att jämföra två strängar utan skiftläge.

+++Syntax

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Strängen som ska jämföras med den första strängen. |

**Exempel**

Följande fråga avgör om personens namn inte är `john`, utan någon skiftlägeskänslighet.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

Använd funktionen `regexGroup` för att extrahera specifik information baserat på det reguljära uttrycket som anges.

+++Syntax

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING}` | Strängen som kontrollen ska utföras på. |
| `{EXPRESSION}` | Det reguljära uttryck som ska matchas mot den första strängen. |
| `{GROUP}` | Uttrycksgrupp att matcha mot. |

**Exempel**

Följande fråga extraherar domännamnet från en e-postadress.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### ersätt {#replace}

Använd funktionen `replace` för att ersätta en given delsträng i en sträng med en annan delsträng.

+++Syntax

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen där delsträngen måste ersättas. |
| `{STRING_2}` | Den delsträng som ska ersättas. |
| `{STRING_3}` | Ersättningsdelsträngen. |

**Exempel**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Returnerar `Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

Använd funktionen `replaceAll` om du vill ersätta alla delsträngar för en text som matchar regex-uttrycket med den angivna literala ersättningssträngen. Regex har en speciell hantering av `\` och `+` och alla regex-uttryck följer PQL escape-strategi. Ersättningen fortsätter från början av strängen till slutet, till exempel om `aa` ersätts med `b` i strängen `aaa` resulterar det i `ba` i stället för `ab`.

+++Syntax

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> När uttrycket som tagits som ett andra argument är ett särskilt regex-tecken använder du ett dubbelt omvänt snedstreck (`//`).  Specialregextecken är: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Läs mer i [Oracle-dokumentation](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### rightTrim {#rightTrim}

Funktionen `rightTrim` tar bort blanksteg från slutet av en sträng.

+++Syntax

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

Funktionen `sha256` beräknar och returnerar sha256-hash för en sträng.

+++Syntax

```sql
{%= sha256(string) %} : string
```

**Exempel**

```sql
{%= sha256("Eliechxh")%}
```

Returnerar `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### dela {#split}

Använd funktionen `split` om du vill dela en sträng med ett visst tecken.

+++Syntax

```sql
{%= split(string,string) %}
```

+++

### beginWith {#startsWith}

Använd funktionen `startsWith` för att avgöra om en sträng börjar med en angiven delsträng.

+++Syntax

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beskrivning |
| --------- | ----------- |
| `{STRING_1}` | Strängen som kontrollen ska utföras på. |
| `{STRING_2}` | Den sträng som ska sökas efter i den första strängen. |
| `{CASE_SENSITIVE}` | En valfri parameter som avgör om kontrollen är skiftlägeskänslig. Som standard är värdet true. |

**Exempel**

Följande fråga avgör, med skiftlägeskänslighet, om personens namn börjar med `Joe`.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

Funktionen `stringToDate` konverterar ett strängvärde till ett datum/tid-värde. Den har två argument: strängbeteckning för ett datum- och tidsvärde samt strängbeteckning för formateringen.

+++Syntax

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exempel**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

Använd funktionen `string_to_integer` för att konvertera ett strängvärde till ett heltalsvärde.

+++Syntax

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Använd funktionen `stringToNumber` för att konvertera en sträng till tal. Den returnerar samma sträng som utdata för ogiltiga indata.

+++Syntax

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Använd funktionen `substr` för att returnera delsträngen för stränguttrycket mellan det inledande indexvärdet och det avslutande indexvärdet.

+++Syntax

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Använd funktionen `titleCase` om du vill att de första bokstäverna i varje ord i en sträng ska skrivas med versaler.

+++Syntax

```sql
{%= titleCase(string) %}
```

**Exempel**

Om personen bor i Washington high street returnerar den här funktionen `Washington High Street`.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Använd funktionen `toBool` för att konvertera ett argumentvärde till ett booleskt värde, beroende på dess typ.

+++Syntax

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Använd funktionen `toDateTime` för att konvertera strängen till ett datum. Det returnerar epokdatumet som utdata för ogiltiga indata.

+++Syntax

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Använd funktionen `toDateTimeOnly` om du vill konvertera ett argumentvärde till ett värde som bara gäller för datum och tid. Det returnerar epokdatumet som utdata för ogiltiga indata. Den här funktionen accepterar fälttyperna string, date, long och integer.

+++Syntax

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trimma {#trim}

Funktionen `trim` tar bort alla blanksteg från början och slutet av en sträng.

+++Syntax

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

Funktionen `upperCase` konverterar en sträng till versaler.

+++Syntax

```sql
{%= upperCase(string) %}
```

**Exempel**

Den här funktionen konverterar profilens efternamn till versaler.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Använd funktionen `urlDecode` för att avkoda en URL-kodad sträng.

+++Syntax

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Använd funktionen `urlEncode` för att koda en sträng som en URL.

+++Syntax

```sql
{%= urlEncode(string) %}: string
```

+++
