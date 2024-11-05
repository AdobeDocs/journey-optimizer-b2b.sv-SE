---
title: Noder för kontoresa
description: Lär dig mer om de nodtyper som du kan använda för att skapa kontoresor i Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: 30075a1804e520b9908ef6b2217a8a91e33e0a84
workflow-type: tm+mt
source-wordcount: '2056'
ht-degree: 0%

---

# Kontoresa noder

När du har [skapat en kontoresa](journey-overview.md#create-an-account-journey) och [lagt till målgruppen](journey-overview.md#add-the-account-audience-for-your-journey) kan du skapa resan med hjälp av noder. Färdkartan är en arbetsyta där du kan skapa flerstegs-B2B-användningsfall för marknadsföring.

Bygg upp din kontoresa genom att kombinera de olika actionnoderna, eventen och orkestreringsnoderna som ett flerstegsscenario för flera kanaler. Varje nod i en resa representerar ett steg längs en logisk väg. Använd följande nodtyper för att skapa en kontoresa:

* [Målgrupp](#account-audience-node)
* [Agera](#take-an-action)
* [Lyssna efter en händelse](#listen-for-an-event)
* [Dela banor](#split-paths)
* [Vänta](#wait)
* [Sammanfoga banor](#merge-paths)

## Nod för målgrupp för konto

Noden [Account Audience](journey-overview.md#add-the-account-audience-for-your-journey) definierar målgruppen för indatakontot (som skapas och hanteras i Adobe Experience Platform) för resan. Den här noden är alltid den första noden och skapas automatiskt som standard.

## Agera

Utför en åtgärd som att skicka ett e-postmeddelande, ändra poängen, tilldela till en köpgrupp och så vidare.

**Åtgärd för konton**: Åtgärden tillämpas på alla personer som är en del av konton på den här sökvägen.

**Åtgärd på personer**: Åtgärden tillämpas på alla personer på den här sökvägen. En åtgärd för personer kan användas inom den delade sökvägen av personer eller dela upp sökväg efter konton.

### Åtgärder och begränsningar {#action-nodes}

| Nodkontext | Åtgärd | Begränsningar |
| ------------ | ------ | ----------- |
| [Personer](#add-a-people-action) | Lägg till i listan | Välj Marketo Engage-arbetsyta<br/>Listnamn |
| | Lägg till i kampanj för begäran om Marketo Engage | Välj arbetsytan Marketo Engage<br/>Välj kampanj för begäran |
| | Tilldela till inköpsgrupp | Välj lösningsintresse<br/>Välj roll |
| | Ändra personpartition i Marketo Engage | Ny partition |
| | Ändra poäng | Efternamn<br/>Ändra |
| | Personens intressanta stund | Typ<br/>Beskrivning |
| | Ta bort från inköpsgrupp | Välj lösningsintresse |
| | Ta bort från lista | Välj Marketo Engage-arbetsyta<br/>Listnamn |
| | Skicka e-post | Skapa nytt e-postmeddelande<br/>Välj e-post från Marketo Engage |
| | Skicka SMS | Skapa SMS |
| [Konton](#add-an-account-action) | Datavärde för kontoändring | Välj attribut<br/>Nytt värde |
| | Intressant stund för konto | Typ (e-post, milstolpe eller webb)<br/>Beskrivning (valfritt) |
| | Lägg till konto på (annan) resa | Välj Live Account Journey |
| | Ta bort konto från resa | Välj Live Account Journey |
| | Skicka försäljningsvarning | Välj lösningsintresse<br/>Skicka e-post till |
| | Uppdatera inköpsgruppsstatus | Välj lösningsintresse<br/>Status (krävs, max 50 tecken) |

### Lägg till en kontoåtgärd

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Take an action]**.

   ![Lägg till kundtjänstnod - delade sökvägar](./assets/add-node-action.png){width="400"}

1. Välj **[!UICONTROL Accounts]** för åtgärden i nodegenskaperna till höger.

1. Välj en åtgärd i listan och ange värden för åtgärden.

   ![Resensnod - utför en åtgärd på ett konto](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Lägga till en personåtgärd

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Take an action]**.

1. Välj **[!UICONTROL People]** för åtgärden i nodegenskaperna till höger.

1. Välj en åtgärd i listan och ange värden för åtgärden.

![Resensnod - utför en åtgärd på personer](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Lyssna efter en händelse

Flytta er målgrupp framåt till nästa steg i kundresan när en händelse inträffar.

* Du kan också definiera hur lång tid resan väntar på den här händelsen. Resan avslutas efter en timeout.
* Dessutom kan du välja att lägga till andra noder på tidsgränsen.

**Lyssna på händelser på konton**: Om minst en person från ett konto utlöser en händelse, går kontot vidare till nästa steg på resan.

**Lyssna på händelser på personer**: Händelser på personer kan bara tillämpas på en kontosökväg. Den är inte tillgänglig för delning via personnod.

### Händelser och begränsningar {#event-nodes}

| Nodkontext | Händelse | Begränsningar |
| ------------ | ----- | ----------- |
| [Personer](#add-a-people-event) | Tilldelad till inköpsgrupp | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <ul><li>Roll</li><li>Aktivitetsdatum</li></ul><br/>Timeout (valfritt) |
| | Klicka på länken i e-postmeddelandet | E-post<br/>Ytterligare begränsningar (valfritt): <ul><li>Länk</li><li>Länk-ID</li><li>Är mobil enhet</li><li>Enhet</li><li>Plattform</li><li>Webbläsare</li><li>Är prediktivt innehåll</li><li>Är robotaktivitet</li><li>Punktaktivitetsmönster</li><li>Webbläsare</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li></ul><br/>Timeout (valfritt) |
| | Klicka på länken i SMS | E-post<br/>Ytterligare begränsningar (valfritt):<ul><li>Länk</li><li>Enhet</li><li>Plattform</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li></ul><br/>Timeout (valfritt) |
| | Ändringar av datavärde | Personattribut<br/>Ytterligare begränsningar (valfritt):<ul><li>Nytt värde</li><li>Föregående värde</li><li>Orsak</li><li>Källa</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li></ul><br/>Timeout (valfritt) |
| | Öppnar e-post | E-post<br/>Ytterligare begränsningar (valfritt): <ul><li>Länk</li><li>Länk-ID</li><li>Är mobil enhet</li><li>Enhet</li><li>Plattform</li><li>Webbläsare</li><li>Är prediktivt innehåll</li><li>Är robotaktivitet</li><li>Punktaktivitetsmönster</li><li>Webbläsare</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li></ul><br/>Timeout (valfritt) |
| | Borttagen från inköpsgrupp | Lösning, intresse<br/>Aktivitetsdatum (valfritt)<br/>Tidsgräns (valfritt) |
| | Poängen har ändrats | Efternamn<br/>Ytterligare begränsningar (valfritt):<ul><li>Ändra</li><li>Nytt musikspår</li><li>Akut</li><li>Prioritet</li><li>Relativ poäng</li><li>Relativ brådska</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li></ul><br/>Timeout (valfritt) |
| | SMS-studsar | SMS<br/>Ytterligare begränsningar (valfritt):<ul><li>Aktivitetsdatum</li><li>Minsta antal gånger</li></ul><br/>Timeout (valfritt) |
| [Konton](#add-an-account-event) | Kontot hade en intressant stund | Typ (e-post, milstolpe eller webb)<br/>Ytterligare begränsningar (valfritt):<ul><li>Beskrivning</li><li>Källa</li><li>Aktivitetsdatum</li></ul> <br/>Timeout (valfritt) |
| | Ändra värde för kontodata | Attribut<br/>Ytterligare begränsningar (valfritt):<ul><li>Nytt värde</li><li>Föregående värde</li><li>Aktivitetsdatum</li></ul> <br/>Timeout (valfritt) |
| | Ändring i inköpsgruppsstatus | Intresse av lösning<br/>Ytterligare begränsningar (valfritt):<ul><li>Ny status</li><li>Föregående status</li><li>Aktivitetsdatum</li></ul><br/> Timeout (valfritt) |
| | Ändrad slutförandepoäng | Intresse av lösning<br/>Ytterligare begränsningar (valfritt):<ul><li>Nytt musikspår</li><li>Föregående poäng</li><li>Aktivitetsdatum</li></ul><br/> Timeout (valfritt) |
| | Ändrad engagemangspoäng | Intresse av lösning<br/>Ytterligare begränsningar (valfritt):<ul><li>Nytt musikspår</li><li>Föregående poäng</li><li>Aktivitetsdatum</li></ul><br/> Timeout (valfritt) |

### Lägg till en kontohändelse

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Listen for an event]**.

1. Välj **[!UICONTROL Accounts]** som händelsetyp i nodegenskaperna till höger.

   ![Resensnod - lyssna på händelser på konto](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Välj en händelse i listan.

1. Klicka på **[!UICONTROL Edit event]** och definiera information för händelsen.

### Lägg till en personhändelse

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Listen for an event]**.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

   ![Resensnod - lyssna på händelser på personer](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Välj en händelse i listan.

1. Klicka på **[!UICONTROL Edit event]** och definiera information för händelsen.

### Lägga till en timeout i en händelsnod

Ange vid behov hur lång tid resan väntar på händelsen. Resan avslutas efter en timeout.

1. Aktivera timeout-växlingen.

1. Välj hur länge resan väntar på att en händelse ska inträffa innan den inträffar.

   Du kan välja att avsluta banan här eller utföra en annan åtgärd genom att ange en annan bana.

1. Om du vill skapa en ny sökväg under resan där du kan lägga till åtgärder och händelser som gäller konton när händelsen inte inträffar, markerar du kryssrutan **[!UICONTROL Set timeout path]**.

   ![Resans händelsnod - ange tidsgräns](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Dela banor

Dela målgruppen baserat på filtervillkor.

>[!NOTE]
>
>Högst 25 banor stöds.

**Dela sökvägar efter konton**: Sökvägar som delas efter konton kan innehålla både konto- och personåtgärder samt händelser. Dessa banor kan delas upp ytterligare.

_Hur fungerar en delad sökväg efter kontonod?_

* När du lägger till en delad sökvägsnod och väljer _Konto_ innehåller varje sökväg som läggs till en slutnod med möjlighet att lägga till noder i varje kant.
* Det går att dela upp sökvägen med konton upprepade gånger, t.ex. på ett kapslat sätt. En delad bana innehåller ett alternativ för att inte lägga till standardbanan.
* Om ett konto/en person inte är berättigad till en av de delade vägarna flyttas den inte framåt under resan.
* Dessa sökvägar kan kombineras med en sammanfogningsnod.

![Resensnod - dela sökvägar efter konto](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Dela banor efter personer**: Banor som delas av personer och kan endast innehålla personåtgärder. Dessa banor kan inte delas igen och kopplas automatiskt tillbaka.

_Hur fungerar en delad sökväg efter personnod?_

* Delad bana efter personnoder är grupperade noder. De sammanfogas automatiskt så att alla personer i publiken kan gå vidare till nästa steg utan att tappa kontexten för de konton de tillhör.
* Delad sökväg för personer kan inte kapslas. Du kan inte lägga till delad sökväg för personer på en sökväg som finns i den här grupperade noden.
* Delad bana innehåller ett alternativ för att inte lägga till en standardbana. Konton/personer som inte är kvalificerade flyttar inte framåt på resan.

![Resensnod - dela sökvägar efter personer](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Sökvillkor {#path-conditions}

| Nodkontext | Sökvillkor | Beskrivning |
| ------------ | --------------- | ----------- |
| [Personer](#add-a-split-path-by-people-node) | [!UICONTROL Person Attributes] | Attribut från personprofilen, inklusive: <ul><li>Ort</li><li>Land</li><li>Födelsedatum</li><li>E-postadress</li><li>Ogiltig e-postadress</li><li>E-postmeddelandet har pausats</li><li>Förnamn</li><li>Ingångsregion</li><li>Befattning</li><li>Efternamn</li><li>Mobiltelefonnummer</li><li>Telefonnummer</li><li>Postnummer</li><li>Stat</li><li>Avprenumererad</li><li>Orsak till avbeställning</li></ul> |
| | [!UICONTROL Activity history] > [!UICONTROL Email] | E-postaktiviteter som är kopplade till resan: <ul><li>[!UICONTROL Clicked link in email]</li><li>Öppen e-post</li><li>Levererades via e-post</li><li>Har skickats e-post</li></ul> Dessa villkor utvärderas med hjälp av ett markerat e-postmeddelande från tidigare under resan. |
| | [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | En värdeändring har gjorts för ett markerat personattribut. De här ändringstyperna är: <ul><li>Nytt värde</li><li>Föregående värde</li><li>Orsak</li><li>Källa</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li></ul> |
| | [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Intressanta händelser som definieras i den associerade Marketo Engage-instansen. Begränsningarna är: ul><li>Milstolpe</li><li>E-post</li><li>Webb</li></ul> |
| | [!UICONTROL Special filters] > [!UICONTROL Member of Buying Group] | Personen är eller är inte medlem i en inköpsgrupp och utvärderas utifrån ett eller flera av följande kriterier: <ul><li>Intresse av lösningar</li><li>Status för inköpsgrupp</li><li>Slutförandepoäng</li><li>Engagement Score</li><li>Roll</li></ul> |
| [Konton](#add-a-split-path-by-account-node) | Kontoattribut | Attribut från kontoprofilen, inklusive: <ul><li>Årliga intäkter</li><li>Ort</li><li>Land</li><li>Medarbetarstorlek</li><li>Bransch</li><li>Namn</li><li>SIC-kod</li><li>Stat</li></ul> |
| | [!UICONTROL Special filters] > [!UICONTROL Has Buying Group] | Kontot har eller saknar medlemmar i inköpsgrupper utvärderade utifrån ett eller flera av följande kriterier: <ul><li>Intresse av lösningar</li><li>Status för inköpsgrupp</li><li>Slutförandepoäng</li><li>Engagement Score</li></ul> |

### Lägg till en delad sökväg efter kontonod

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Split paths]**.

   ![Lägg till kundtjänstnod - delade sökvägar](./assets/add-node-split.png){width="300"}

1. I nodegenskaperna till höger väljer du **[!UICONTROL Accounts]** för delningen.

1. Om du vill definiera ett villkor som gäller för _[!UICONTROL Path 1]_klickar du på&#x200B;**[!UICONTROL Apply condition]**.

   ![Delad sökvägsnod - lägg till villkor](./assets/node-split-properties-apply-condition.png){width="500"}

1. I villkorsredigeraren lägger du till ett eller flera filter för att definiera den delade banan.

   * Dra och släpp filterattribut från den vänstra navigeringen och slutför matchningsdefinitionen.

   * Finjustera dina villkor genom att använda **[!UICONTROL Filter logic]** överst. Du väljer att matcha alla attributvillkor eller alla villkor.

     ![Delad sökvägsnod - logik för villkorsfilter](./assets/node-split-conditions.png){width="700" zoomable="yes"}

   * Klicka på **[!UICONTROL Done]**.

1. Om du vill lägga till fler sökvägar klickar du på **[!UICONTROL Add path]** och upprepar de föregående stegen för att lägga till villkor som gäller för den här sökvägen.

   Du kan också etikettera varje bana baserat på dessa villkor eller använda standardetiketterna.

1. (Valfritt) Lägg till en standardsökväg för konton som inte är kvalificerade för de andra sökvägarna. Annars avslutas resan för dessa konton.

   ![Egenskaper för delad sökvägsnod - andra konton](./assets/node-split-properties-other-accounts.png){width="700" zoomable="yes"}

### Lägga till en delad sökväg efter personnod

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Split paths]**.

   ![Lägg till kundtjänstnod - delade sökvägar](./assets/add-node-split.png){width="300"}

1. I nodegenskaperna till höger väljer du **[!UICONTROL People]** för delningen.

1. Om du vill definiera ett villkor som gäller för _[!UICONTROL Path 1]_klickar du på&#x200B;**[!UICONTROL Apply condition]**.

1. I villkorsredigeraren lägger du till ett eller flera filter för att definiera den delade banan.

   * Dra och släpp filterattribut från den vänstra navigeringen och slutför matchningsdefinitionen.

   * Finjustera dina villkor genom att använda **[!UICONTROL Filter logic]** överst. Du väljer att matcha alla attributvillkor eller alla villkor.

   * Klicka på **[!UICONTROL Done]**.

1. Om du vill lägga till fler sökvägar klickar du på **[!UICONTROL Add path]** och upprepar de föregående stegen för att lägga till villkor som gäller för den här sökvägen.

   Du kan också etikettera varje bana baserat på dessa villkor eller använda standardetiketterna.

1. Slutligen kan du lägga till en standardsökväg för personer som inte är kvalificerade för ovanstående sökvägar. Annars slutar resan för dessa människor

När du har definierat villkor för varje bana för att dela din publik på personnivå, kan du lägga till åtgärder som du vill ska utföras på personer.

>[!NOTE]
>
>När du delar målgruppen efter personer kan du bara lägga till åtgärder för personer.

## Vänta

Vänta en viss tid innan du går vidare till nästa steg.

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Wait]**.

1. I nodegenskaperna till höger anger du **[!UICONTROL Duration]** tid att vänta innan resan fortsätter till nästa nod i sökvägen.

![Resensnod - vänta](./assets/node-wait.png){width="700" zoomable="yes"}

## Sammanfoga banor

Olika sökvägar i din resa kan sammanfogas och göras osammanfogade med den här noden.

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Split paths]**.

1. Klicka på den delade noden för att öppna dess egenskaper till höger.

1. Klicka på [!UICONTROL Add path] om du vill skapa tre banor.

1. Lägg till en kombination av åtgärder och händelser i varje sökväg.

1. Klicka på plusikonen ( **+** ) för någon av dessa banor och välj **[!UICONTROL Merge]** bland de visade alternativen.

   ![Resensnod - sammanfoga banor](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Markera de banor som du vill sammanfoga i egenskaperna för sammanfogningsnoden.

   ![Resensnod - sammanfoga banor](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Nu sammanfogas banorna så att konton från de markerade banorna kombineras till en enda bana som kan fortsätta genom resan.

1. Om det behövs kan du dela upp sökvägarna genom att gå tillbaka till egenskaperna för sammanfogningsnoden och avmarkera kryssrutan för de sökvägar som du vill ta bort.
