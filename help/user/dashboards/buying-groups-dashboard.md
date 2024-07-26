---
title: Instrumentpanel för översikt över inköpsgrupper
description: Lär dig mer om kontrollpanelen för inköpsgruppsöversikt och hur den aktiverar försäljningsleveransen från marknadsföringsteamet.
feature: Dashboards, Buying Groups
exl-id: 26b1e7fd-2252-4782-8d0f-874720cc7d03
source-git-commit: c5fe3f1530b2c3d9b9eab8ad089dbab9a2c74e99
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Instrumentpanel för översikt över inköpsgrupper

Kontrollpanelen för överblick över inköpsgrupp är utformad för B2B-försäljningsprocessen. Marknadsföringsteamet kan dela _klara_ inköpsgrupper och deras medlemmar tillsammans med viktiga data till säljteamet för utförande. Denna process säkerställer en smidig övergång från marknadsföring till försäljning.

Försäljningen omfattar följande:

* **Data Handoff**: Marknadsföring identifierar _ready_ -måldata och gör den tillgänglig för Försäljning i CSV-format. 
* **Försäljningsgodkännande**: Försäljningen granskar manuellt och inkluderar _klara_ mål i sin pipeline.

## Status för inköpsgrupp

Få insikter om hur inköpsgrupperna utvecklas i vyn Köpgruppsstatus. Den här visualiseringen visar distributionen av dina inköpsgrupper, kategoriserade efter deras senaste statusuppdatering inom en angiven tidsram.

![Översikt över inköpsgrupper](./assets/buying-groups-overview.png){width="800" zoomable="yes"}

**[!UICONTROL Status]** (y-axel): Spåra resan för inköpsgrupper genom olika faser.
**[!UICONTROL Number of Buying Groups]** (x-axel): Kvantifiera antalet inköpsgrupper vid varje status, vilket ger en tydlig uppskattning av din trattes hälsa och aktivitet.
<!-- To generate a shareable PDF of your current view, click **[!UICONTROL Export]** at the top-right corner of the page. -->

### Datafiltrering

* **Datafilter** - Använd _[!UICONTROL Date filter]_, som visar ändringsdatumet för senaste status för inköpsgruppen. Startdatumet kan justeras. Slutdatumet är som standard den aktuella dagen.

  ![Filtrerar statusdata för inköpsgrupp efter datumintervall](./assets//buying-group-status-filter-date.png){width="400"}

* **Attributfilter** - Klicka på ikonen _Filter_ längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

   * Intresse av lösningar
   * Status
   * Status för inköpsgrupp
   * Kontoregion
   * Kontobransch
  <!-- * Account's Industry -->

  ![Filtrerar statusdata för inköpsgrupp efter attribut](./assets/buying-group-status-drill-through-filters.png){width="500"}

## Engagera med data

Använd åtgärdsmenyn i det övre högra hörnet när du vill interagera med data.

![Klicka på ikonen för att komma åt åtgärdsmenyn](./assets/buying-group-more-menu.png){width="400"}

### [!UICONTROL Drill through]

Välj **[!UICONTROL Drill through]** om du vill ha en ingående analys av enskilda gruppstatusar.

![Detaljnivån för diagramdata](./assets/buying-group-status-drill-through-view.png){width="600" zoomable="yes"}

De globala filter som används på kontrollpanelen överförs och kan inte ändras från den här sidan.

Klicka på ikonen för åtgärdsmenyn längst upp till höger och välj **[!UICONTROL View more]** för att [visa utökade data och insikter](#view-more).

### [!UICONTROL View more]

Välj **[!UICONTROL View more]** om du vill ha utökade data och insikter. Popup-fönstret som visas innehåller ett diagram och en tabell som visar hur inköpsgruppens status är fördelad:

* [!UICONTROL Account ID ]
* [!UICONTROL Account Name]
* [!UICONTROL Account Region]
* [!UICONTROL Account Industry]
* [!UICONTROL Buying Group Name]
* [!UICONTROL Solution Interest]
* [!UICONTROL Status]
* [!UICONTROL Engagement Score]
* [!UICONTROL Completeness Score]
* [!UICONTROL Member Role]
* [!UICONTROL Member Enrolled / Created Date]
* [!UICONTROL Person ID]
* [!UICONTROL Name]
* [!UICONTROL Email]
* [!UICONTROL Title]
* [!UICONTROL Number of Inbound Engagement Activities]
* [!UICONTROL Last engagement date]

![Visa utökade data](./assets/buying-group-status-view-more.png){width="600" zoomable="yes"}

Om du vill hämta data klickar du på **[!UICONTROL Download CSV]** i det övre högra hörnet.
