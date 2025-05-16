---
title: Köpgrupper
description: Läs om hur köpgrupper i Journey Optimizer B2B edition kan öka marknadsföringens effektivitet genom att identifiera och inrikta sig på medlemmar i era kontolistor.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: d1130841ed3c560208bc93c53a54169f9b0b94aa
workflow-type: tm+mt
source-wordcount: '1756'
ht-degree: 7%

---


# Köpgrupper

För B2B-försäljnings- och marknadsföringsaktiviteter är konton avgörande för alla strategier. Varje konto har en grupp som är kopplad till det, och dessa personer kan vara anställda på kontot eller entreprenörer som arbetar med kontot. Konton är hierarkiska och olika produkter kan säljas på olika nivåer i hierarkin. Adobe Experience Platform kan till exempel säljas på företagsnivå till ett konto på den högsta nivån. Och Adobe Photoshop kan säljas till ett konto som representerar en avdelning eller avdelning inom en organisation, t.ex. en designavdelning inom ett större företag.

![Diagram över kontoroller](assets/account-roles-diagram.png){width="800"}

I kontot kan det finnas en delmängd av personer som utgör _köpgruppen_. Dessa personer fattar i slutändan inköpsbeslutet, så de behöver särskild uppmärksamhet från marknadsföraren och kan behöva annan information som skickas till dem än de andra som är kopplade till kontot. Köpgrupper kan bestå av olika grupper av personer för olika produktlinjer eller erbjudanden. En cybersäkerhetsprodukt kan t.ex. kräva en Chief Information Officer eller Chief Security Officer och en representant från den juridiska avdelningen för att godkänna ett inköp, men en buggspårningsprodukt kan vanligtvis ha en VP som Engineering och en IT-chef som medlemmar i inköpsgruppen.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Se videoöversikten](#overview-video)

## Viktiga komponenter

Ni kan öka marknadsföringens effektivitet genom att inrätta inköpsgrupper i Journey Optimizer B2B edition som identifierar saknade medlemmar i era målkontolistor baserat på de lösningar som era säljteam ansvarar för. Innan du och ditt marknadsföringsteam börjar skapa inköpsgrupper måste du se till att du har definierat nyckelkomponenterna. De här komponenterna är viktiga för att ni ska kunna uppnå era affärsmål.

| Komponent | Syfte |
| --------- | ------- |
| Intresse av lösningar | Den här komponenten ger svaret på: <ul><li>Vad säljer du som marknadsföringsorganisation?</li><li>Vilken produkt eller produktsamling riktar ni er till?</li></ul>  **_Exempel:_** Merförsäljning av nya produkter X till befintliga kunder |
| Målgrupp | Den här komponenten ger svaret på: <ul><li>Till vem säljer du?</li><li>Vad är listan med konton som ni riktar er mot?</li></ul> **_Exempel:_** Kontosegment som definieras av konton med produkt Y som har intäkter över 1 miljon |
| Köpa grupprollsmallar | Den här komponenten ger svaret på: <ul><li>Vilka roller riktar ni er mot?</li><li>Vilken uppsättning regler används för att avgöra vem som har tilldelats till inköpsgrupproller?</li></ul>  **_Exempel:_** Tilldela en person med CMO-titel rollen beslutsfattare |
| Köpgruppsfaser | (Valfritt) Den här komponenten ger svaret på: Hur lyckas eller misslyckas inköpsgruppen? |

## Arbetsflöde för inköpsgrupp

1. Skapa inköpsgrupper.

   * Definiera [lösningsintresse](./solution-interests.md) och [rollmall](./buying-groups-role-templates.md)
   * [Skapa inköpsgruppen](./buying-groups-create.md#create-buying-groups) och tilldela [inköpsgruppfaser](./buying-group-stages.md).

1. Identifiera saknade personer.

   Analysera inköpsgruppen med hjälp av filter.

   **_Exempel:_** Beslutsfattarrollen saknas och poängen för fullständighet är &lt; 50

1. Slutför definitioner av inköpsgrupper.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Använd inköpsgruppen på dina kontoresor.

## Visa inköpsgrupper och komponenter

Expandera **[!UICONTROL Accounts]** till vänster och klicka på **[!UICONTROL Buying groups]**.

Sidan _[!UICONTROL Buying groups]_&#x200B;är ordnad som flikar:

| Tabb | Beskrivning |
| --- | ----------- |
| [!UICONTROL Overview] | Den här fliken är standard och visar kontrollpanelen [Köpgrupper](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga inköpsgrupper. </li><li>Sök genom att köpa gruppnamn. </li><li>Filtrera efter lösningsintresse. </li><li>Granska om du vill köpa gruppinformation. </li><li>Skapa en inköpsgrupp. </li></ul> |
| [!UICONTROL Solution interests] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga inköpsgrupper. </li><li>Sök genom att köpa gruppnamn. </li><li>Få tillgång till och redigera egenskaper för lösningsintresse. </li><li>Skapa ett intresse för en lösning. </li><li>Ta bort ett lösningsintresse. </li><li>Visa och ta bort inköpsgruppjobb. </li></ul> |
| [!UICONTROL Roles Templates] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga rollmallar. </li><li>Sök efter rollmallens namn. </li><li>Få åtkomst till och redigera egenskaper och villkor för rollmallar. </li><li>Skapa en rollmall. </li><li>Ta bort en rollmall. </li></ul> |
| [!UICONTROL Stages] | Fliken har stöd för följande aktiviteter: <ul><li>Visa den befintliga inköpsgruppsmodellen. </li><li>Få åtkomst till och redigera utkasten till inköpsgruppfasmodell. </li><li>Skapa inköpsgruppens fasmodell. </li></ul> |

## Köpa gruppsökning och filter

Använd fliken _[!UICONTROL Browse]_&#x200B;för att visa listan över inköpsgrupper. Du kan söka efter namn och filtrera listan efter lösningsintresse.

![Buying group browse page](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Information om inköpsgrupp

Om du vill få tillgång till information om en inköpsgrupp klickar du på namnet på inköpsgruppen på fliken _[!UICONTROL Browse]_. [Läs mer](./buying-group-details.md)

![Information om inköpsgrupp](assets/buying-group-details.png){width="600" zoomable="yes"}

### Poäng för slutförande av inköpsgrupp

Slutpoängen används för att avgöra om inköpsgruppen är fullständig, vilket innebär att den har rätt medlemmar tilldelade till rollerna och är klar att användas i en kontoresa. Poängen är en procentandel som baseras på antalet roller i inköpsgruppen och hur många roller som tilldelas med minst en lead.

Om det till exempel finns fyra roller inom en inköpsgrupp och tre av de fyra rollerna tilldelas till minst en lead, är inköpsgruppen 75 % färdig.

Slutresultatet för inköpsgruppen beräknas om varje gång en inköpsgrupp skapas eller uppdateras.

### Köpa poäng för gruppengagemang

Att köpa poäng för gruppengagemang är en siffra som avgör engagemanget hos medlemmarna i en inköpsgrupp, baserat på de aktiviteter de utför.

* Beräkningen av poäng för engagemang börjar så snart inköpsgruppen genereras.
* Alla inkommande aktiviteter som utförts av medlemmarna i inköpsgruppen under de senaste 30 dagarna används för att beräkna poängen.
* Med 30-dagarsfönstret och när aktiviteter förfaller kan poängen sänkas.
* Det finns ett dagligt frekvenstak på 20 för varje aktivitet. Om en medlem i en inköpsgrupp utför samma aktivitet mer än 20 gånger per dag, begränsas antalet aktiviteter till 20 och inte ett högre antal.
* Den poäng som visas är avrundad. Ett resultat på till exempel 75,89999 visas som 76.

+++aktiviteter som används för poängsättning

| Aktivitetsnamn | Beskrivning | Typ av åtagande | Maximalt antal dagliga frekvenser | Aktivitetsvikt |
| --- | --- | --- | --- | --- |
| Registrera dig för event | Registrerar för en händelse som är associerad med en kampanj | Händelse | 20 | 60 |
| Delta händelse | Deltar i en kampanjhändelse | Händelse | 20 | 90 |
| Öppna e-post | Öppnar ett e-postmeddelande | E-post | 20 | 30 |
| Klicka på E-post | Klicka på en länk i ett e-postmeddelande | E-post | 20 | 30 |
| Open Sales Email | Öppnar ett e-postmeddelande | E-post | 20 | 30 |
| Klicka på E-postadress | Klicka på en länk i ett e-postmeddelande | E-post | 20 | 30 |
| Intressant stund | Har ett intressant ögonblick | Kuraterad | 20 | 60 |
| Tryck på push-meddelande | Tar emot ett push-meddelande | Mobil | 20 | 30 |
| Mobilappsaktivitet | Utför en aktivitet i en mobilapp | Mobil | 20 | 30 |
| Mobilappssession | Är aktiv i mobilappssession | Mobil | 20 | 30 |
| Fyll i formulär för leadannonser på Facebook | Fyller i och skickar in ett leadannonsformulär på en Facebook-sida | Social | 20 | 30 |
| Klicka på RTP-anrop för åtgärd | Klicka på en personlig uppmaning | Webb | 20 | 60 |
| Visa meddelande i appen | Visar ett meddelande i appen | Mobil | 20 | 30 |
| Tryck på meddelande i appen | Tryck på ett meddelande i appen | Mobil | 20 | 30 |
| Prenumerera på SMS | Prenumererar på SMS-kommunikation | SMS | 20 | 90 |
| Svara på e-postadress | Svar på ett e-postmeddelande | E-post | 20 | 30 |
| Engagerad med en dialogruta | Deltar i en Dynamic Chat-dialog | Chatt | 20 | 90 |
| Interagera med dokument i dialogrutan | Interagera med ett dokument i en Dynamic Chat-dialogruta | Chatt | 20 | 90 |
| Schemalagt möte i dialogrutan | Schemalägger ett möte i en Dynamic Chat-dialogruta | Chatt | 20 | 90 |
| Dialogrutemål som nåtts | Uppnå ett mål i en Dynamic Chat-dialogruta |  | 20 | 90 |
| Svar på en omröstning i webbinariet | Svar på en omröstning i ett webbinarium | Chatt | 20 | 90 |
| Call to action clicked in webbinar | Klicka på en länk för att ringa till åtgärd i ett webbinarium | Utlysning | 20 | 30 |
| Resurshämtningar i webbinarium | Hämtar en fil/resurs i ett webbinarium | Händelse | 20 | 60 |
| Frågor och svar i webbinarium | Frågar frågor i ett webbinarium | Händelse | 20 | 60 |
| Har övervakad händelse | Deltog i en händelse | Händelse | 20 | 60 |
| Aktiverat med en agent i dialogrutan | Aktiverar en agent i en Dynamic Chat-dialog | Chatt | 20 | 90 |
| Klicka på Länk i chatt i dialogrutan | Klicka på en länk i en Dynamic Chat-dialogruta | Chatt | 20 | 90 |
| Engagerad med ett konversationsflöde | Engagerar med ett Dynamic Chat-konverteringsflöde | Chatt | 20 | 90 |
| Schemalagt möte i konversationsflöde | Schemalägger en avtalad tid i ett samtal med Dynamic Chat | Chatt | 20 | 90 |
| Målet för konversationsflöde har uppnåtts | Uppfyller ett mål i ett Dynamic Chat-konversationsflöde | Chatt | 20 | 90 |
| Interagera med dokument i konversationsflöde | Interagera med ett dokument i ett Dynamic Chat-konversationsflöde | Chatt | 20 | 90 |
| Engagerad med en agent i konversationsflöde | Engagerar med en agent i ett Dynamic Chat-konversationsflöde | Chatt | 20 | 90 |
| Klicka på Länk i chatt i konversationsflöde | Klicka på en länk i ett Dynamic Chat-konversationsflöde | Chatt | 20 | 90 |
| Klicka på Länk i SMS V2 | Klicka på en länk i ett SMS-meddelande | SMS | 20 | 90 |

>[!NOTE]
>
>Aktiviteter för engagemangsmusik registreras i Marketo Engage [aktivitetsloggen för en person](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}.

+++

#### Viktning

Användare kan tilldela _viktning_ till varje roll i rollmallen för att tilldela olika vikter för en roll för att beräkna förlovningspoängen.

![Ange viktning för varje roll i rollmallen](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Varje viktningsnivå motsvarar ett värde som används för att beräkna engagemangspoängen:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Minor] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Important] = 80
* [!UICONTROL Vital] = 100

En rollmall med tre roller viktade som _[!UICONTROL Vital]_,_[!UICONTROL Important]_ och _[!UICONTROL Normal]_&#x200B;konverteras till följande viktade procentandelar:

| Roll | Viktning | Systemvärde | Värdeberäkning | Procent |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Beslutsfattare | Vital | 100 | 100/240 | 41,67 % |
| Påverkande | Viktigt | 80 | 80/240 | 33,33 % |
| Yrkesverksamma | Normal | 60 | 60/240 | 25 % |
|               | Totalt | 240 |                   |           |

#### Exempel på beräkning

I följande exempel visas beräkningen av engagemangspoängen med den angivna rollviktsprocenten, antalet inkommande aktiviteter för varje medlem i köpgruppen och ett dagligt tak på 20 antal för varje händelse (om det har inträffat flera gånger).

| Roll | medlem | Typ av aktivitet | Gårdagens antal | Antal i dag | Beräkning | Totalt antal poäng |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Beslutsfattare | Adam | Besökt webbplats | 37 | 15 | 20 + 15 | 35 |
|               |          | E-post som klickats | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Märk | Besökt webbplats | 5 | 3 | 5 + 3 | 8 |
|               |          | E-post som klickats | 1 | 1 | 1 + 1 | 2 |
|               |          | Nedladdad pub | 3 | 2 | 3 + 2 | 5 |
| **Totalpoäng för beslutsfattare** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Påverkande | John | Besökt webbplats | 19 | 9 | 19 + 9 | 28 |
| **Påverkar totalpoäng** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Yrkesverksamma | Bob | E-post som klickats | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | E-post som klickats | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | E-post som klickats | 1 | 1 | 1 + 1 | 2 |
|               |          | Besökt webbplats | 1 | 7 | 1 + 7 | 8 |
|               |          | Nedladdad pub | 1 | 2 | 1 + 2 | 3 |
| **Totalt antal praktikanter** |         |             |                 |             |      | **17** |

Det slutliga poängtalet för engagemang beräknas genom att viktningen tillämpas för varje rollpoäng:

| Roll | Rolltotalpoäng | Rollvikt i % | Poäng X vikt % |
|-------------- |---------------- |------------- |---------------- |
| Beslutsfattare | 52 | 41,67 % | 21,67 |
| Påverkande | 28 | 33,33 % | 9,33 |
| Yrkesverksamma | 17 | 25 % | 4,25 |
| **Slutgiltigt engagemangsmoment** |                |             | **35.25** |

## Videoöversikt

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
