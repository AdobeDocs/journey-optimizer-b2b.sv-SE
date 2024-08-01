---
title: Köpgrupper
description: Läs om hur du köper grupper och deras komponenter.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 4%

---


# Köpgrupper

För B2B-försäljnings- och marknadsföringsaktiviteter är konton avgörande för alla strategier. Varje konto har en grupp som är kopplad till det, och dessa personer kan vara anställda på kontot eller entreprenörer som arbetar med kontot. Konton är hierarkiska och olika produkter kan säljas på olika nivåer i hierarkin. Adobe Experience Platform kan till exempel säljas på företagsnivå till ett toppnivåkonto, medan Adobe Photoshop kan säljas till ett konto som representerar en avdelning eller avdelning inom en organisation, till exempel en designavdelning inom ett större företag.

![Diagram över kontoroller](assets/account-roles-diagram.png){width="800"}

I kontot kan det finnas en delmängd av personer som utgör _köpgruppen_. Dessa personer är de som i slutändan fattar inköpsbeslutet, så de behöver särskild uppmärksamhet från marknadsföraren och kan behöva annan information som skickas till dem än de andra som är kopplade till kontot. Köpgrupper kan bestå av olika grupper av personer för olika produktlinjer eller erbjudanden. En cybersäkerhetsprodukt kan t.ex. kräva en Chief Information Officer eller Chief Security Officer och en representant från den juridiska avdelningen för att godkänna ett inköp, men en buggspårningsprodukt kan vanligtvis ha en VP of Engineering och en IT Director som medlemmar i inköpsgruppen.

## Viktiga komponenter

Ni kan öka marknadsföringens effektivitet genom att inrätta inköpsgrupper i Journey Optimizer B2B Edition som identifierar saknade medlemmar i era målkonton baserat på de lösningar som era säljteam ansvarar för. Innan du och ditt marknadsföringsteam börjar skapa inköpsgrupper måste du se till att du har definierat nyckelkomponenterna. De här komponenterna är viktiga för att ni ska kunna uppnå era affärsmål.

| Komponent | Syfte |
| --------- | ------- |
| Intresse av lösningar | Den här komponenten ger svaret på: <ul><li>Vad säljer du som marknadsföringsorganisation?</li><li>Vilken produkt eller produktsamling riktar ni er till?</li></ul>  **_Exempel:_** Merförsäljning av nya produkter X till befintliga kunder |
| Målgrupp | Den här komponenten ger svaret på: <ul><li>Till vem säljer du?</li><li>Vad är listan med konton som ni riktar er mot?</li></ul> **_Exempel:_** Kontosegment som definieras av konton med produkt Y som har intäkter över 1 miljon |
| Köpa grupprollsmallar | Den här komponenten ger svaret på: <ul><li>Vilka roller riktar ni er mot?</li><li>Vilken uppsättning regler används för att avgöra vem som har tilldelats till inköpsgrupproller?</li></ul>  **_Exempel:_** Tilldela en person med CMO-titel rollen beslutsfattare |

## Arbetsflöde för inköpsgrupp

1. Skapa inköpsgrupper.

   Alternativ:
   * Använd [lösningsintresse](./solution-interests.md) och [rollmall](./buying-groups-role-templates.md)
   * Använda import från tredje part
   * Generera från AI/ML

1. Identifiera saknade personer.

   Analysera inköpsgruppen med hjälp av filter.

   **_Exempel:_** Beslutsfattarrollen saknas och poängen för fullständighet är &lt; 50

1. Slutför definitioner av inköpsgrupper.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Använd för en kontoresa via de kopplade lösningsintressena.

## Få tillgång till inköpsgrupper och komponenter

Expandera **[!UICONTROL Accounts]** till vänster och klicka på **[!UICONTROL Buying groups]**.

Sidan _[!UICONTROL Buying groups]_är ordnad som flikar:

| Tabb | Beskrivning |
| --- | ----------- |
| [!UICONTROL Overview] | Den här fliken är standard och visar kontrollpanelen [Köpgrupper](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga inköpsgrupper. </li><li>Sök genom att köpa gruppnamn. </li><li>Filtrera efter lösningsintresse. </li><li>Granska om du vill köpa gruppinformation. </li><li>Skapa en inköpsgrupp. Ta bort en inköpsgrupp.</li></ul> |
| [!UICONTROL Solution interests] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga inköpsgrupper. </li><li>Sök genom att köpa gruppnamn. </li><li>Få tillgång till och redigera egenskaper för lösningsintresse. </li><li>Skapa ett intresse för en lösning. </li><li>Ta bort ett lösningsintresse. </li><li>Visa och ta bort inköpsgruppjobb. </li></ul> |
| [!UICONTROL Roles Templates] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga rollmallar. </li><li>Sök efter rollmallens namn. </li><li>Få åtkomst till och redigera egenskaper och villkor för rollmallar. </li><li>Skapa en rollmall. </li><li>Ta bort en rollmall. </li></ul> |

## Köpa gruppsökning och filter

Använd fliken _[!UICONTROL Browse]_för att visa listan över inköpsgrupper. Du kan söka efter namn och filtrera listan efter lösningsintresse.

![Buying group browse page](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Information om inköpsgrupp

Om du vill få tillgång till information om en inköpsgrupp klickar du på namnet på inköpsgruppen på fliken _[!UICONTROL Browse]_.

![Information om inköpsgrupp](assets/buying-group-details.png){width="600" zoomable="yes"}

### Poäng för slutförande av inköpsgrupp

Slutpoängen används för att avgöra om inköpsgruppen är fullständig, vilket innebär att den har rätt medlemmar tilldelade till rollerna och är klar att användas i en kontoresa. Poängen är en procentandel som baseras på antalet roller i inköpsgruppen och hur många roller som tilldelas med minst en lead.

Om det till exempel finns fyra roller inom en inköpsgrupp och tre av de fyra rollerna tilldelas till minst en lead, är inköpsgruppen 75 % färdig.

Slutresultatet för inköpsgruppen beräknas om varje gång en inköpsgrupp skapas eller uppdateras.

### Köpa poäng för gruppengagemang

Poängen för engagemang används för att utvärdera effekten av era marknadsföringsprogram baserat på att köpa gruppbeteenden som spåras över resorna. Denna poäng härleds från aktivitet under de senaste 30 dagarna. Alla rolländringar i en mall kräver omberäkning av engagemangspoängen för alla inköpsgrupper som skapats med den mallen. Endast inkommande aktiviteter utvärderas vid beräkning av en engagemangspoäng.

Den visade poängen avrundas nedåt (till exempel visas poängen 75,89999 som 76), det finns ingen övre gräns för poängen för GA och det finns en daglig frekvensgräns på 20.

I följande exempel visas beräkningen av poängen för engagemang:

**Buying group 1** - engagement score = 22.15

| Användare | Roll | Rollvikt | Åtgärd | Idag | Igår | Åtgärdsbredd | Poäng |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Adam | Beslutsfattare | 80% | Besökt webbplats | 1000 | 2 | 1 | 22 |
| | | | E-post som klickades | 1 | 0 | 1 | 1 |
| | | | Nedladdad pub | 1 | 3 | 1 | 4 |
| Bob | Påverkande | 15 % | Besökt webbplats | 1 | 2 | 1 | 3 |
| Calvin | Yrkesverksamma | 5 % | Besökt webbplats | 1 | 1 | 1 | 2 |

**Buying group 2** - engagement score = 8.55

| Användare | Roll | Rollvikt | Åtgärd | Idag | Igår | Åtgärdsbredd | Poäng |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Alvin | Beslutsfattare | 80% | Besökt webbplats | 3 | 2 | 1 | 5 |
| | | | E-post som klickades | 1 | 0 | 1 | 1 |
| | | | Nedladdad pub | 1 | 3 | 1 | 4 |
| Bret | Påverkande | 15 % | Besökt webbplats | 1 | 2 | 1 | 3 |
| Cam | Yrkesverksamma | 5 % | Besökt webbplats | 1 | 1 | 1 | 2 |
