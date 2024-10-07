---
title: E-postmeddelande om försäljning
description: Lär dig hur du tar med ett automatiskt försäljningsmeddelande i dina kontoresor.
feature: Email Authoring, Content
exl-id: 01bffbce-6c73-483a-8731-de4e5569cf61
source-git-commit: 33bd8f68ae581d974fc52f94df6f2249d9493325
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# E-postmeddelande om försäljning

Ett _försäljningsvarningsmeddelande_ signalerar att inköpsgrupper har skickats till försäljning. E-postmeddelandet innehåller en sammanfattning av inköpsgruppen och information om medlemmarna i inköpsgruppen och deras aktiviteter.

Som marknadsförare kan du konfigurera en e-postnod för försäljningsavisering på dina kontoresor för att informera säljteamet om att resan för vissa inköpsgrupper har slutförts. I noden kan du ange e-postadresserna till säljteamet eller ett distributionsalias som når en uppsättning konton.

## E-postinnehåll

+++Exempel på försäljningsmeddelande via e-post
![Exempel på ett e-postmeddelande om försäljning med standardmallen](./assets/sales-alert-email-example.png){width="500" zoomable="yes"}

+++

| Avsnitt | Namn | Beskrivning |
| - | ---- | ----------- |
| Information om inköpsgrupp | Namn på inköpsgrupp | Visningsnamn för inköpsgruppen. |
|   | Kontonamn | Namn på kontot. |
|   | Engagement score | Inköpsteamet baserat på aktiva interaktionsaktiviteter de senaste 30 dagarna. |
|   | Slutförandepoäng | Inköpsgruppens slutresultat. |
|   | Intresse av lösningar | Intressen av lösningar kopplade till inköpsgruppen |
|   | Status | Status för inköpsgruppen. |
| Köpgrupper i korthet | Ledande medlemmar | De mest engagerade medlemmarna i inköpsgruppen genom att köpa gruppmedlemmens engagemangspoäng och roll. |
|   | Intresseämne | De vanligaste nyckelorden i innehållsengagemanget, baserat på e-post, nedladdningar, chatt, PDF-granskning, aktivitetssammanfattning och webbinarifrågor. |
|   | Saknade roller | Obligatoriska roller i mallen men saknas i inköpsgruppen. |
| Sammanfattning av inköpsgrupper | Sammanfattning av aktivitet (drivs av generativ AI) | AI-genererad sammanfattning av inköpsgruppen baserad på medlemmarnas aktiviteter. De senaste 30 dagarnas verksamhet beaktas. |
|   | Viktiga ögonblick | Nyligen intressanta stunder relaterade till medlemmarna i inköpsgruppen. |
| Medlemmar | Lista över fyra köpmedlemmar | Information om de fyra främsta medlemmarna i inköpsgruppen efter interaktionspoäng och roll. |
| Varje medlem i en inköpsgrupp | Medlemsnamn | Namn på inköpsgruppsmedlemmen. |
|   | Titel | Namn på köpgruppsmedlemmen. |
|   | Roll | Medlemmens köpgruppsroll. |
|   | Engagement score | Köper gruppmedlemmens engagemangspoäng. Poängen baseras på aktiva engagemangsaktiviteter de senaste 30 dagarna. |
|   | Senaste intressanta stund | Det senaste intressanta tillfället som rör medlemmen. |
|   | De senaste aktiviteterna | De senaste två aktiviteterna som är kopplade till medlemmarna i inköpsgruppen. |
|   | E-post-ID | E-post-ID för köpgruppsmedlemmen. |
|   | Telefonnummer | Telefonnummer till inköpsgruppsmedlemmen. |

## Lägg till en e-poståtgärd för försäljningsavisering i en kontoresa

Du kan konfigurera e-postleveranser för försäljningsaviseringar under en kontoresa när du lägger till en _[!UICONTROL Take an action]_-nod och gör följande:

1. Välj **[!UICONTROL Account]** för målet _[!UICONTROL Action on]_.

1. Välj **[!UICONTROL Send Sales Alert]** för _[!UICONTROL Action on accounts]_.

1. För **[!UICONTROL Select solution interest]** väljer du det lösningsintresse som ska användas för det genererade e-postinnehållet.

1. För **[!UICONTROL Send Email To]** anger du varje e-postadress eller alias som du vill ta med för leveransen.

   ![Skapa ny e-postdialogruta](assets/sales-alert-email-journey-node.png){width="600" zoomable="yes"}

   När kontoresan har publicerats levereras försäljningsmeddelandet enligt dessa parametrar.
