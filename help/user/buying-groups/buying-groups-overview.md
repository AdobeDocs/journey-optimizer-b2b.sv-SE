---
title: Köpgrupper
description: Läs om hur köpgrupper i Journey Optimizer B2B edition kan öka marknadsföringens effektivitet genom att identifiera och inrikta sig på medlemmar i era kontolistor.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: eb80b57b0481837a50c7c0985ac4dc5d71f3577e
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 0%

---


# Köpgrupper

För B2B-försäljnings- och marknadsföringsaktiviteter är konton avgörande för alla strategier. Varje konto har en grupp som är kopplad till det, och dessa personer kan vara anställda på kontot eller entreprenörer som arbetar med kontot. Konton är hierarkiska och olika produkter kan säljas på olika nivåer i hierarkin. Adobe Experience Platform kan till exempel säljas på företagsnivå till ett konto på den högsta nivån. Och Adobe Photoshop kan säljas till ett konto som representerar en avdelning eller avdelning inom en organisation, t.ex. en designavdelning inom ett större företag.

![Diagram över kontoroller](assets/account-roles-diagram.png){width="800"}

I kontot kan det finnas en delmängd av personer som utgör _köpgruppen_. Dessa personer fattar i slutändan inköpsbeslutet, så de behöver särskild uppmärksamhet från marknadsföraren och kan behöva annan information som skickas till dem än de andra som är kopplade till kontot. Köpgrupper kan bestå av olika grupper av personer för olika produktlinjer eller erbjudanden. En cybersäkerhetsprodukt kan till exempel kräva en informationschef eller Chief Security Officer och en representant från den juridiska avdelningen för att godkänna ett inköp. En produkt för buggspårning kan normalt ha en VP av Engineering och en IT-chef som medlemmar i inköpsgruppen.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Se videoöversikten](#overview-video)

## Viktiga komponenter

Ni kan öka marknadsföringens effektivitet genom att inrätta inköpsgrupper i Journey Optimizer B2B edition som identifierar medlemmar i era målkontolistor för de lösningar som era säljteam ansvarar för. Innan du och ditt marknadsföringsteam börjar skapa inköpsgrupper måste du se till att du har definierat nyckelkomponenterna. De här komponenterna är viktiga för att ni ska kunna uppnå era affärsmål.

| Komponent | Syfte |
| --------- | ------- |
| Intresse av lösningar | Den här komponenten ger svaret på: <ul><li>Vad säljer du som marknadsföringsorganisation?</li><li>Vilken produkt eller produktsamling riktar ni er till?</li></ul>  **_Example:_** Merförsäljning av nya produkter X till befintliga kunder |
| Målgrupp | Den här komponenten ger svaret på: <ul><li>Till vem säljer du?</li><li>Vad är listan med konton som ni riktar er mot?</li></ul> **_Example:_** Kontosegment som definieras av konton med produkt Y som har intäkter över 1 miljon |
| Köpa grupprollsmallar | Den här komponenten ger svaret på: <ul><li>Vilka roller riktar ni er mot?</li><li>Vilken uppsättning regler används för att avgöra vem som har tilldelats till inköpsgrupproller?</li></ul>  **_Exempel:_** Tilldela en person med CMO-titel rollen beslutsfattare |
| Köpgruppsfaser | (Valfritt) Den här komponenten ger svaret på: Hur lyckas eller misslyckas inköpsgruppen? |

## Medlemstilldelning

Det finns tre sätt att tilldela eller ta bort medlemmar från en inköpsgrupp. I följande lista beskrivs dessa additions- och borttagningsmetoder i prioritetsordning. Den översta metoden har högsta prioritet och den understa kan inte åsidosätta den.

1. **_Manuell åtgärd_** - En manuell åtgärd för att lägga till eller ta bort medlem som har utförts av en försäljningsanvändare för inköpsgruppen
2. **_Reseåtgärd_** - Resa [åtgärdsnoder för köp av gruppmedlemskap](../journeys/action-nodes.md#add-a-people-based-action) (_Tilldela till inköpsgrupp_ eller _Ta bort från inköpsgrupp_)
3. **_Systemjobb_** - Buying group [creation](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) och underhållsjobb.

För att undvika att en medlemsuppgift åsidosätts felaktigt i en inköpsgrupp ligger listan i prioritetsordningen som följs i systemet för att säkerställa korrekt medlemstilldelning. Om en försäljningsanvändare till exempel lägger till en medlem i inköpsgruppen manuellt, vill de inte att ett underhållsjobb ska ändra tillägget. Följande scenarier används med hjälp av prioritetsordningen:

* Om en användare tilldelar en medlem manuellt till en inköpsgrupp, och den följs av ett underhållsjobb för inköpsgrupp som tar bort samma medlem från inköpsgruppen, tar underhållsjobbet **inte bort** den medlemmen och kan inte åsidosätta den manuella tilldelningen.
* Om en användare tilldelar en medlem manuellt till en inköpsgrupp, och den följs av en utlösad kundnod som tar bort samma medlem från inköpsgruppen, tar inte nodåtgärden **bort** den medlemmen och kan inte åsidosätta den manuella tilldelningen.
* Om en utlöst transportåtgärdsnod lägger till en medlem i en inköpsgrupp, och den följs av ett underhållsjobb för inköpsgrupp som tar bort samma medlem från inköpsgruppen, tar underhållsjobbet **inte bort** den medlemmen och kan inte åsidosätta reseåtgärdstilldelningen.

## Arbetsflöde för inköpsgrupp

1. Skapa inköpsgrupper.

   * Definiera [lösningsintresse](./solution-interests.md) och [rollmall](./buying-groups-role-templates.md)
   * [Skapa inköpsgruppen](./buying-groups-create.md#create-buying-groups) och tilldela [inköpsgruppfaser](./buying-group-stages.md).

1. Identifiera saknade personer genom fullständighet.

   Analysera inköpsgruppen med hjälp av filter.

   **_Example:_** Beslutsfattarrollen saknas och poängen för fullständighet är &lt; 50

1. Slutför definitioner av inköpsgrupper.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Lägg till inköpsgruppåtgärder på dina kontoresor.

## Visa inköpsgrupper och komponenter

Expandera **[!UICONTROL Accounts]** till vänster och klicka på **[!UICONTROL Buying groups]**.

Sidan _[!UICONTROL Buying groups]_är ordnad som flikar:

| Tabb | Beskrivning |
| --- | ----------- |
| [!UICONTROL Overview] | Den här fliken är standard och visar kontrollpanelen [Köpgrupper](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga inköpsgrupper. </li><li>Sök efter inköpsgruppens namn. </li><li>Filtrera efter lösningsintresse. </li><li>Granska om du vill köpa gruppinformation. </li><li>Skapa en inköpsgrupp. </li></ul> |
| [!UICONTROL Solution interests] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga inköpsgrupper. </li><li>Sök efter inköpsgruppens namn. </li><li>Få tillgång till och redigera egenskaper för lösningsintresse. </li><li>Skapa ett intresse för en lösning. </li><li>Ta bort ett lösningsintresse. </li><li>Visa och ta bort inköpsgruppjobb. </li></ul> |
| [!UICONTROL Roles Templates] | Fliken har stöd för följande aktiviteter: <ul><li>Visa listan över befintliga rollmallar. </li><li>Sök efter rollmallens namn. </li><li>Få åtkomst till och redigera egenskaper och villkor för rollmallar. </li><li>Skapa en rollmall. </li><li>Ta bort en rollmall. </li></ul> |
| [!UICONTROL Stages] | Fliken har stöd för följande aktiviteter: <ul><li>Visa den befintliga inköpsgruppsmodellen. </li><li>Få åtkomst till och redigera utkasten till inköpsgruppfasmodell. </li><li>Skapa inköpsgruppens fasmodell. </li></ul> |

## Köpa gruppsökning och filter

Använd fliken _[!UICONTROL Browse]_för att visa listan över inköpsgrupper. Du kan söka efter namn och filtrera listan efter lösningsintresse.

![Buying group browse page](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Information om inköpsgrupp

Om du vill få tillgång till information om en inköpsgrupp klickar du på namnet på inköpsgruppen på fliken _[!UICONTROL Browse]_. [Läs mer](./buying-group-details.md)

![Information om inköpsgrupp](assets/buying-group-details.png){width="600" zoomable="yes"}

### Poäng för slutförande av inköpsgrupp

Slutenhetspoängen används för att avgöra om inköpsgruppen har rätt medlemmar tilldelade till rollerna och är klar att användas i en kontoresa. Poängen är en procentandel som baseras på antalet roller i inköpsgruppen och hur många roller som tilldelas med minst en lead.

Om det till exempel finns fyra roller inom en inköpsgrupp och tre av de fyra rollerna tilldelas till minst en lead, är inköpsgruppen 75 % färdig.

Slutresultatet för inköpsgruppen beräknas om varje gång en inköpsgrupp skapas eller uppdateras.

### Köpa poäng för gruppengagemang {#engagement-score}

Poängen för engagemang baseras på aktiviteter för köpgruppsmedlemmar, viktade åtgärder och viktade roller. Resultatpoängen normaliseras inom klienten/instansen för att möjliggöra en konsekvent jämförelse och möjliggöra åtgärdbara insikter.

Den inledande poängberäkningen för engagemang börjar så snart du skapar inköpsgruppen och beräknas om dagligen.

Mer information om aktiviteter och beräkningar finns i [Resultat för engagemang](./engagement-scores.md).

## Videoöversikt

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
