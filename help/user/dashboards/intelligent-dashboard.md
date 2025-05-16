---
title: Intelligent Dashboard
description: Läs mer om Intelligent Dashboard som ger en heltäckande bild av mätvärden för inköpsgrupper och konton
feature: Dashboards, Intelligent Insights, Buying Groups
role: User
exl-id: 671a78d2-613c-4ac8-bef8-08c673173c72
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---

# Intelligent Dashboard

Den intelligenta Dashboard ger en heltäckande bild av kundgruppens och kontots mätvärden, vilket hjälper er att övervaka och strategiska era marknadsföringssatsningar mer effektivt.

Om du vill komma åt _Intelligent Dashboard_ markerar du **[!UICONTROL Dashboard]**-objektet i den vänstra navigeringen.

![Öppna den intelligenta instrumentpanelen](./assets/intelligent-dashboard.png){width="800" zoomable="yes"}

Den intelligenta kontrollpanelen ger även åtkomst till konto- och köpgruppsinformationssidor som innehåller två typer av generativa AI-funktioner:

* Sammanfattningar för konton och inköpsgrupper
* Avsiktsidentifiering för person, inköpsgrupp och konto

{{intent-data-note}}

För att kunna använda den information och de insikter som finns i den intelligenta kontrollpanelen måste Journey Optimizer B2B edition-instansen ha de nödvändiga objekten på plats:

| Typ | Krav |
| ---- | ----------- |
| [Köper gruppfaser](#buying-group-stages) | Ställ in inköpsgruppfaserna **och** lägga till i skapade inköpsgrupper. |
| [Köp av grupphögdagrar](#buying-group-highlights) | Ställ in inköpsgruppfaserna **och** lägga till i skapade inköpsgrupper. |
| [Kontoökning](#surging-accounts) | En eller flera publicerade resor **eller** skapade inköpsgrupper. |
| [Kontohögdagrar](#account-highlights) | En eller flera publicerade resor **eller** skapade inköpsgrupper. |
| [Kontakttäckning](#contact-coverage) | En eller flera skapade inköpsgrupper (faser behövs inte). |
| [Kontaktöverlappning](#contact-overlap) | En eller flera skapade inköpsgrupper (faser behövs inte). |
| [Sidan med kontoinformation](../accounts/account-details.md) | En eller flera publicerade resor. |
| [Buying group detail page](../buying-groups/buying-group-details.md) | En eller flera skapade inköpsgrupper (faser behövs inte). |

## Köpgruppsfaser {#buying-group-stages}

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_buying_group_stages"
>title="Köpgruppsfaser"
>abstract="I det här diagrammet visas en översikt över hur inköpsgrupper fortskrider i olika faser baserat på de konfigurerade övergångsreglerna. Den första raden visar antalet inköpsgrupper i ett visst steg på det första datumet i den valda tidsramen jämfört med det sista datumet i den valda tidsramen."

Diagrammet _[!UICONTROL Buying Group Stages]_&#x200B;ger en översikt över hur inköpsgrupper fortskrider i olika faser ([baserat på övergångsregler som har konfigurerats av en administratör](../buying-groups/buying-group-stages.md)).

>[!NOTE]
>
>Tillgängligheten för inköpsgruppfaser kräver att inköpsgruppfaserna konfigureras. Se [Köpa gruppfaser](../buying-groups/buying-group-stages.md) för detaljerad information om faser och hur du definierar och aktiverar faser för inköpsgrupper.

![Köper datavisualisering för gruppfaser](./assets/intelligent-dashboards-buying-group-stages.png){width="800" zoomable="yes"}

I diagrammet används inköpsgruppfaserna från den senast publicerade versionen av inköpsgruppens fasmodell. Det finns två staplar för varje scen. Den första raden visar antalet inköpsgrupper på det första datumet i den valda tidsramen. Och det andra (i jämförelse) är antalet inköpsgrupper på det sista datumet i tidsramen. Du kan hålla muspekaren över varje fält för att se antalet inköpsgrupper i varje fas.

![Håll pekaren över fältet om du vill visa detaljerade siffror](./assets/intelligent-dashboard-buying-group-stages-hover-bar.png){width="400"}

### Generativ AI-sammanfattning

Klicka på ett fält för att visa en generativ AI-sammanfattning av inköpsgrupper i det steget för den valda tidsperioden.

![Klicka på fältet för att visa en generativ AI-sammanfattning](./assets/intelligent-dashboard-buying-group-stages-click-bar.png){width="500"}

Den genererade sammanfattningen ger en översikt över hur inköpsgrupper fortskrider i olika faser baserat på de konfigurerade övergångsreglerna.

### Tidsperiod {#time-period-stages}

Använd datumfiltret längst upp till höger för att ändra datumintervallet för datavisualiseringar. Klicka på nedåtpilen för att ange ett relativt datumintervall eller för att ange anpassade start- och slutdatum.

<!-- ![Filtering tdata by date range](./assets/intelligent-dashboard-date-filter.png){width="300"} -->

### Attributfilter {#attribute-filter-stages}

Klicka på ikonen _Filter_ ( ![ikonen Redigera](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Konto
* Scennamn

<!-- Add screen when the UI is available ![Filtering the buying group status data by attribute](./assets/buying-group-status-drill-through-filters.png){width="500"} -->

## Köpgrupper i korthet {#buying-group-highlights}

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_buying_group_highlights_engagement"
>title="De fem populäraste inköpsgrupperna efter engagemang"
>abstract="De mest engagerade inköpsgrupperna baserat på deras normaliserade engagemangspoäng."

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_buying_group_highlights_velocity"
>title="De fem snabbaste köpgrupperna"
>abstract="Köpgrupper baserat på hur snabbt de utvecklas stegvis."

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_buying_group_highlights_stagnant"
>title="De fem viktigaste köpgrupperna"
>abstract="Fantastiska inköpsgrupper som inte går igenom alla faser trots höga slutresultat."

Avsnittet _[!UICONTROL Buying group highlights]_&#x200B;är organiserat i tre rader för att visa information om inköpsgrupper av intresse för din organisation.

![Köp av grupphögdagrar](./assets/intelligent-dashboard-buying-group-highlights.png){width="800" zoomable="yes"}

* **De fem populäraste inköpsgrupperna efter engagemang** - Den här raden visar de högst engagerade inköpsgrupperna baserat på deras normaliserade engagemangspoäng.
* **De fem populäraste köpgrupperna med hög hastighet** - På den här raden visas de främsta köpgrupperna baserat på hur snabbt de går igenom inköpsgruppsfaserna.
* **De fem populäraste mellanliggande inköpsgrupperna** - Den här raden visar de mest mellanliggande inköpsgrupperna som inte går igenom faser trots ett högt slutresultat.

Varje kort innehåller följande data:

* **_Buying group name_**. Klicka på namnet för att öppna sidan med information om inköpsgrupper.
* **_Kontonamn_**. Klicka på namnet för att öppna kontodetaljsidan (hyperlänkad till kontodetaljsidan).
* **_Aktuell fas_** för inköpsgruppen.
* **_Aktivitetspoäng_** (normaliserat för alla inköpsgrupper). Om alla inköpsgrupper har samma högsta poäng visas den senaste uppdaterade poängen.
* **_Slutförandepoäng_** (från 1-100). Om alla inköpsgrupper har samma högsta poäng visas den senaste uppdaterade poängen.
* **_Kategoriåtergivning_**. Klicka på _[!UICONTROL View details]_&#x200B;för att visa återgivningsdata:

  ![Köper gruppåtergivningsdata](./assets/intelligent-dashboard-buying-group-intent-details.png){width="500" zoomable="yes"}

   * I informationsfönstret visas kategorinamnet med återgivningsnivån högst upp.
   * Data för varje rad är ordnade i kolumner: produktnamn, produktintent-styrka och nyckelord högst upp efter intent-strength.
   * Sorteringsordningen är hög till låg för kategori, produkt och nyckelord. Om en eller flera av typerna har samma återgivningsstyrka används alfabetisk ordning i sorteringen.

  {{intent-data-note}}

Klicka på **[!UICONTROL View All]** längst upp till höger på panelen _Om du vill köpa en grupp markeras_ klickar du på  för att navigera till listsidan för köpgrupper.

### Attributfilter {#attribute-filter-bg-highlights}

Klicka på ikonen _Filter_ ( ![ikonen Redigera](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Köpgrupp
* Konto

<!-- Add screen when the UI is available ![Filtering the buying group status data by attribute](./assets/buying-group-status-drill-through-filters.png){width="500"} -->

### Tidsperiod {#time-period-bg-highlights}

Använd datumfiltret längst upp till höger för att ändra datumintervallet för datavisualiseringar. Klicka på nedåtpilen för att ange ett relativt datumintervall eller för att ange anpassade start- och slutdatum.

<!-- ![Filtering tdata by date range](./assets/intelligent-dashboard-date-filter.png){width="300"} -->

## Efterföljande konton {#account-surge}

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_account_surge"
>title="Kontoökning"
>abstract="Konton med stor förändring i engagemanget inom den valda tidsramen."

Avsnittet _[!UICONTROL Surging accounts]_&#x200B;visar en visualisering av kontona med en betydande förändring i engagemanget inom den valda tidsramen.

>[!NOTE]
>
>Data för kontoökning är begränsade till konton som Journey Optimizer B2B edition har tagit in på en kontomrets resa eller via inköpsgrupper.

![Datavisualisering för kontoökning](./assets/intelligent-dashboard-account-surge.png){width="800" zoomable="yes"}

Håll pekaren över varje fält för att visa antalet konton i varje kategori.

![Håll pekaren över fältet för att visa de detaljerade siffrorna](./assets/intelligent-dashboard-account-surge-hover-bar.png){width="400"}

Klicka på ett fält för att visa en generativ AI-sammanfattning av kontona i kategorin för den valda tidsramen.

![Klicka på fältet för att visa en generativ AI-sammanfattning](./assets/intelligent-dashboard-account-surge-click-bar.png){width="500"}

### Attributfilter {#attribute-filter-acct-surge}

Klicka på ikonen _Filter_ ( ![ikonen Redigera](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Bransch
* Län

<!-- Add screen when the UI is available ![Filtering the buying group status data by attribute](./assets/buying-group-status-drill-through-filters.png){width="500"} -->

### Tidsperiod {#time-period-acct-surge}

Använd datumfiltret längst upp till höger för att ändra datumintervallet för datavisualiseringar. Klicka på nedåtpilen för att ange ett relativt datumintervall eller för att ange anpassade start- och slutdatum.

<!-- ![Filtering tdata by date range](./assets/intelligent-dashboard-date-filter.png){width="300"} -->

## Kontohögdagrar {#account-highlights}

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_account_highlights_surging"
>title="Efterföljande konton"
>abstract="Konton med avsevärt ökat engagemang i den valda tidsramen "

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_account_highlights_at_risk"
>title="Riskkonton"
>abstract="Konton med en avsevärd minskning av engagemangets drivkraft under den valda tidsramen."

Avsnittet _[!UICONTROL Account highlights]_&#x200B;är indelat i två rader för att visa information om konton av intresse för din organisation.

>[!NOTE]
>
>Data som framhäver kontona är begränsade till konton som är inmatade av Journey Optimizer B2B edition hos en viss kontompubliken via kontoresor eller inköpsgrupper.

![Kontohögdagrar](./assets/intelligent-dashboard-account-highlights.png){width="800" zoomable="yes"}

* **Övergående konton** - Den här raden visar kontona med en betydande ökning av engagemanget under den valda tidsramen.
* **Riskkonton** - Den här raden visar kontona med en betydande minskning av engagemanget under den valda tidsramen.

Varje kort innehåller följande data:

* **_Kontonamn_**. Klicka på namnet för att öppna sidan med kontoinformation.
* **_Generativ AI-sammanfattning_** av kontot.
* **_Nyckelordsmetod_**. Klicka på _[!UICONTROL View details]_&#x200B;för att visa återgivningsdata:

  ![Data för kontoåtergivning](./assets/intelligent-dashboard-account-intent-details.png){width="500" zoomable="yes"}

   * I informationsfönstret visas kategorinamnet med återgivningsnivån högst upp.
   * Data för varje rad är ordnade i kolumner: produktnamn, produktintent-styrka och nyckelord högst upp efter intent-strength.
   * Sorteringsordningen är hög till låg för kategori, produkt och nyckelord. Om en eller flera av typerna har samma återgivningsstyrka används alfabetisk ordning i sorteringen.

  {{intent-data-note}}
<!-- 
At the top right of the _Buying group highlights_ panel, click **[!UICONTROL View All]** to navigate to the Buying groups list page. -->

### Attributfilter {#attribute-filter-acct-highlights}

Klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Köpgrupp

<!-- Add screen when the UI is available ![Filtering the buying group status data by attribute](./assets/buying-group-status-drill-through-filters.png){width="500"} -->

### Tidsperiod {#time-period-acct-highlights}

Använd datumfiltret längst upp till höger för att ändra datumintervallet för datavisualiseringar. Klicka på nedåtpilen för att ange ett relativt datumintervall eller för att ange anpassade start- och slutdatum.

<!-- ![Filtering tdata by date range](./assets/intelligent-dashboard-date-filter.png){width="300"} -->

## Kontakttäckning {#contact-coverage}

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_contact_coverage"
>title="Kontakttäckning"
>abstract="Visar antalet kontakter med en specifik roll som är associerad med ett lösningsintresse. Tilldelningen av roll- och lösningsintressen baseras på köpgruppsmallen."

Avsnittet _[!UICONTROL Contact coverage]_&#x200B;visar en visualisering av antalet kontakter med en specifik roll som är associerad med ett lösningsintresse. Tilldelningen av roll- och lösningsintressen baseras på köpgruppsmallen.

>[!NOTE]
>
>Kontaktuppgifter baseras på de inköpsgrupper som har skapats i Journey Optimizer B2B edition-instansen.

![Datavisualisering för kontoökning](./assets/intelligent-dashboard-contact-coverage.png){width="800" zoomable="yes"}

Håll pekaren över varje cell för att visa antalet kontakter i rollen/lösningsintresset.

![Håll pekaren över fältet för att visa de detaljerade siffrorna](./assets/intelligent-dashboard-contact-coverage-hover-cell.png){width="400"}

Klicka på en cell för att visa detaljerad information om kontakterna i rollen/lösningsintresset.

![Klicka i cellen för att visa kontaktinformation](./assets/intelligent-dashboard-contact-coverage-click-cell.png){width="700" zoomable="yes"}

### Attributfilter {#attribute-filter-contact-coverage}

Klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Konton

<!-- Add screen when the UI is available ![Filtering the buying group status data by attribute](./assets/buying-group-status-drill-through-filters.png){width="500"} -->

## Kontaktöverlappning {#contact-overlap}

>[!CONTEXTUALHELP]
>id="ajo-b2b_intelligent_dashboard_contact_overlap"
>title="Kontaktöverlappning"
>abstract="Lista över kontakter som ingår i mer än en inköpsgrupp som ett resultat av att de är kopplade till flera lösningsintressen."

Avsnittet _[!UICONTROL Contact overlap]_&#x200B;visar en lista med kontakter som är en del av mer än en inköpsgrupp som ett resultat av att de är kopplade till flera lösningsintressen.

>[!NOTE]
>
>Kontaktöverlappningsdata baseras på de inköpsgrupper som skapas i Journey Optimizer B2B edition-instansen.

![Kontaktöverlappningstabell](./assets/intelligent-dashboard-contact-overlap.png){width="800" zoomable="yes"}

Klicka på _Informationsikonen_ ( ![Informationsikonen](../assets/do-not-localize/icon-info.svg) ) om du vill visa en tabell med följande information:

* Köpgruppens namn (klicka på namnet för att öppna sidan med information om inköpsgruppen)
* Roll
* Intresse av lösningar
* Produktåtergivning
* Produkt

![Kontaktöverlappningsinformation](./assets/intelligent-dashboard-contact-overlap-detail-info.png){width="600" zoomable="yes"}

### Attributfilter {#attribute-filter-contact-overage}

Klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Roller
* Konton

<!-- Add screen when the UI is available ![Filtering the buying group status data by attribute](./assets/buying-group-status-drill-through-filters.png){width="500"} -->
