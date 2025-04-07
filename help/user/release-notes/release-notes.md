---
title: Versionsinformation
description: Senaste versionsinformationen för Adobe Journey Optimizer B2B-version
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 228837741f3373ee2b8423515b7412564281f8ea
workflow-type: tm+mt
source-wordcount: '1814'
ht-degree: 4%

---

# Versionsinformation för Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition ger kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar.

Journey Optimizer B2B edition är inbyggt i [!DNL Adobe Experience Platform] och ärver från de senaste innovationerna och förbättringarna. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest){target="_blank"}.

Granska [produktbeskrivningen](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} om du vill ha information om berättiganden, säkerhetsutkast och begränsningar.

## Versionsinformation 2025.3

**Releasedatum**: 1 april 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | Kontolistor | Nu kan du skapa en statisk eller dynamisk kontolista för att rikta in namngivna konton efter dina definierade kriterier, till exempel bransch, plats eller företagets storlek. <a href="../accounts/account-lists.md">Läs mer</a> |
| Ny funktion | Mina token för kontoresor | Nu kan du definiera en uppsättning anpassade tokens med värden som är specifika för kontoresan. Den här uppsättningen anpassade tokens kallas _Mina token_ och någon av dessa anpassade tokens är till för personalisering när du redigerar e-postmeddelanden om resan. <a href="../content/personalization-my-tokens.md">Läs mer</a> |
| Ny funktion | Ta bort inköpsgruppsfaser | Du kan ta bort inköpsgruppens fasmodell när den är i ett utkast eller publicerat tillstånd. Om den publiceras (live) kan du bara ta bort den när den inte är kopplad till ett lösningsintresse. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Läs mer</a> |
| Förbättring | Antal resantnoder | Ökad synlighet i antalet medlemskap på resan på nodnivå. Använd den här informationen för att validera kontostatus under en resa. |

## Versionsinformation 2025.2

**Releasedatum**: 11 mars 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | Anpassningsbara fält - innehållsfragment | Som designer för innehållsfragment kan du ange en parameter för en komponent i fragmentet som redigerbar. Detta gör att e-postförfattaren eller mallskaparen kan ange ett anpassat fältvärde som är specifikt för deras behov. Den här anpassningsflaggan är begränsad till visuella komponenter för bild, text och knappar. <a href="../content/fragment-authoring.md#enable-custom-fields">Läs mer</a> |
| Ny funktion | Inbyggda roller och produktbehörigheter för B2B | Experience Platform innehåller nu en uppsättning inbyggda (standardroller) roller som du kan använda för att hantera åtkomst till B2B-produktfunktionerna. <a href="../admin/user-management.md#b2b-built-in-roles">Läs mer</a> <br/>Administratörer kan nu definiera anpassade roller i Adobe Experience Platform så att Journey Optimizer B2B edition-produktbehörigheter ingår.  <a href="../admin/user-management.md#b2b-product-permissions">Läs mer</a> |
| Ny funktion | Typer av resedubbletter | När du duplicerar en kontoresa kan du inkludera nodinformation, exklusive e-post och SMS-meddelanden som skapats i Journey Optimizer B2B edition. Du kan också skapa en skelettkopia av struktur- och sökvägsflödena utan nodinformation och inställningar. <a href="../journeys/journey-overview.md#duplicate-journey">Läs mer</a> |
| Förbättring | Fyra extra exempel på e-postmallar | Exempelbiblioteket med e-postmallar innehåller nu fyra SecurFinancial-mallar som exempel för återengagemang, information, näring och exempel på feedback |

## Versionsinformation 2025.1 {#Jan-2025}

**Releasedatum**: 6 februari 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | Vidarebefordra upplevelsehändelser | Administratörer kan konfigurera Adobe Experience Platform (AEP)-baserade händelsedefinitioner. Med dessa konfigurationer kan marknadsförare skapa kontoresor som reagerar på AEP Experience Events.  <a href="../admin/configure-aep-events.md">Läs mer</a> |
| Ny funktion | Betalda mediemål | Kvalificera kända personer för betalda mediekampanjer från en kontoresa så att ni kan engagera dem ytterligare på annonsplattformar som LinkedIn. Använd en delad sökvägsnod i en kontoresa för att segmentera målgrupper baserat på specifika beteenden och identifiera konton som motiverar ytterligare engagemang. Lägg sedan till personer från dessa konton till en extern kundpublik via CDP i realtid till ett betalmediemål som stöds. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Läs mer</a> |
| Ny funktion | Intelligent kontrollpanel | Se hur köpgrupperna fortskrider på sina kontoresor, inklusive AI-genererade insikter för mer intelligent analys och korrekt kontoprioritering. <a href="../dashboards/intelligent-dashboard.md">Läs mer</a> |
| Ny funktion | Information om inköpsgrupp och konto | Se insikter på köpgrupps- och kontonivå för att få mer kontext och historiska data när ni börjar engagera en kund.<p>Köpgruppens information innehåller alla tredjepartsmetoder som upptäcks. <a href="../buying-groups/buying-group-details.md">Läs mer</a><p>Kontona för kontoinformation belyser den ökning i engagemang som upptäckts, så att ni kan informera om försäljning på konton som är klara för anpassat säljfokuserat engagemang.  <a href="../accounts/account-details.md">Läs mer</a> |
| Ny funktion | Reseöversikt | När du får åtkomst till kontoresor ger fliken Översikt en omfattande ögonblicksbild av dina aktiva kontoresor, med detaljerad information om kontoförloppet med hjälp av cirkel- och stapeldiagram som kategoriserar och kvantifierar slutföranden samt engagemangsaktiviteter.  <a href="../dashboards/journeys-dashboard.md">Läs mer</a> |
| Ny funktion | Adobe Express bildredigering | Med Adobe Express snabbåtgärder kan du göra enkla redigeringar (till exempel beskära och ändra storlek) av bilder för att få ett mer elegant utseende i ditt innehåll. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Läs mer</a>  <p>För en mer omfattande uppsättning designverktyg ger integreringen en fullständig Adobe Express-licens för Journey Optimizer B2B edition. Med den här konfigurationen blir Adobe Express hela användargränssnitt tillgängligt på den lokala resursytan. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Läs mer</a> |
| Ny funktion | Återgivningsfilter för inköp av grupproller | När du skickar in dina intent-nyckelord förutser Intent Detection-modellen en lösning/produkt av intresse med tillräcklig säkerhet baserat på en leads aktivitet. <a href="../admin/intent-data.md">Läs mer</a> <p>Den här återgivningsinformationen är tillgänglig för att definiera villkor för inköpsgrupproller <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Läs mer</a> |
| Förbättring | Stöd för Marketo Engage event under resor | Noden _Lyssna efter händelse_ har nu stöd för två Marketo Engage-händelser på personnivå: _Besökswebbsida_ och _Fyller i formulär_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Läs mer</a> |
| Förbättring | Köpa gruppfilter för Marketo Engage smarta listor | Visa och skapa smarta listor med inköpsgruppsfilter i Marketo Engage. Med dessa filter kan ni inaktivera och inkludera köp av gruppmedlemmar i Marketo Engage-kampanjer och program från kontoresor inom Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Läs mer</a> |
| Förbättring | Marketo Engage listmedlemsfilter för resor och roller | I Journey Optimizer B2B kontrollerar du om Marketo Engage-listmedlemskap är ett villkor för en _delad sökväg av personnoden_ för att undvika dubbletter i reseaktiviteter. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Läs mer</a> <p> Använd listmedlemskap som rollvillkor när du köper grupprollmallar. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Läs mer</a> |
| Förbättring | Instrumentpanel för översikt av engagemang | Kontrollpanelen uppdateras för att ge en heltäckande bild av engagemanget. Här visas realtidsstatistik över konton och enskilda interaktioner genom snapshot circle-diagram och trendavslöjande linjediagram över tiden. <a href="../dashboards/engagement-dashboard.md">Läs mer</a> |


## Versionsinformation oktober 2024 {#Oct-2024}

**Releasedatum**: 29 oktober 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | Villkorligt innehåll i e-postmallar | Anpassa ert e-postinnehåll baserat på mottagarnas beteende och profilegenskaper - både på konto- och lead-nivå. <p>När du skapar ett e-postmeddelande för din kontoresa i den visuella e-postdesignrymden kan du använda villkorsregler för att definiera flera varianter för valfri innehållskomponent. <a href="../content/conditional-content.md">Läs mer</a> |
| Ny funktion | _Lägg till i listan_ och _Ta bort från listan_ personåtgärder i resor | Anpassa ert e-postinnehåll baserat på mottagarnas beteende och profilegenskaper - både på konto- och lead-nivå. <a href="../journeys/action-nodes.md">Läs mer</a> |
| Ny funktion | Innehållsstyrning och låsning av komponenter | Om du vill vara säker på att du följer godkända innehållsdesigner kan du använda funktioner för innehållsstyrning för att låsa innehållskomponenter i e-postmallar. När innehållsstyrning är aktiverat i e-postmallen kan marknadsförarna bara ändra de tillåtna elementen för att se till att det är i linje med innehållsstrategin. <a href="../content/template-content-governance.md">Läs mer</a> |
| Ny funktion | Köpgruppsfaser | När du definierar och publicerar en anpassad testmodell för inköpsgrupper kan du följa upp köpgruppsutvecklingen genom inköpsgruppens livscykelfaser. Använd de här faserna för att identifiera nästa bästa åtgärd för medlemmar i inköpsgrupper. Du konfigurerar övergångsreglerna och resenoderna som bestämmer scenens förlopp och utlöser åtgärder baserat på ändringar. <a href="../buying-groups/buying-group-stages.md">Läs mer</a> |
| Förbättring | Nya färdiga e-postmallar | Exempelmallsbiblioteket innehåller nu ytterligare e-postmallar som utformats för B2B-marknadsförare. Använd de här exempelmallarna som utgångspunkt och lägg till egna varumärken och meddelanden. <a href="../content/email-templates.md#select-a-design-template">Läs mer</a> |
| Förbättring | Anpassade fält som personattribut | Om du har definierat anpassade personfält i kontots målgruppsschema i Experience Platform är dessa fält även tillgängliga som personattribut under villkor. Använd dessa anpassade attribut i: <li>Rollmallar <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Läs mer</a></li><li>Dela banor efter personresenoder <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Läs mer</a></li> |
| Förbättring | Inställningar för e-postkanal | E-postinställningarna visas nu i Journey Optimizer B2B edition-gränssnittet. Du kan snabbt granska aktuella konfigurationer och administratörer kan klicka på _[!UICONTROL Edit settings]_för att gå direkt till inställningarna i Marketo Engage och uppdatera dem enligt organisationens krav. <a href="../admin/configure-channels-emails.md">Läs mer</a> |

## Versionsinformation september 2024 {#Sept-2024}

**Releasedatum**: 7 oktober 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Förbättring | Bibliotek för centrala resurser | Med det förbättrade biblioteket för _centrala resurser_ kan du använda alla bildresurser i din Marketo Engage-instans på Design Studio-arbetsytorna. Det finns inbyggda skyddsfunktioner som förhindrar redigering av Marketo Engage-resurser från Journey Optimizer B2B edition samt borttagning och flytt. Dessa skydd säkerställer att källmaterialet (Marketo Engage Design Studio) bevaras samtidigt som det går att läsa och återanvända i Journey Optimizer B2B edition.<p>För resurser som endast är avsedda att användas i Journey Optimizer B2B edition har en specifik arbetsyta fullständiga funktioner för resurshantering. <a href="../content/marketo-engage-design-studio.md">Läs mer</a> |
| Ny funktion | Senast använda resurser | Hemsidan i Journey Optimizer B2B edition-appen innehåller nu avsnittet _[!UICONTROL Recently accessed]_, som innehåller en lista över de senast använda resurserna för marknadsföraren eller administratören. Du kan använda den här listan för att gå direkt till resursen som du nyligen arbetade med utan att navigera genom en serie resurssidor och söka. <p>Listan innehåller ytterligare information om ändringen så att du kan bestämma vilken av resurserna som behöver ändras ytterligare från det senaste mötet. För e-postresurser visas den kontoresa där e-postresursen används. <a href="../home-page.md">Läs mer</a> |
| Förbättring | Delad resenod - ändra ordning på banor | I noder med delade sökvägar utvärderas banfiltreringen i uppifrån och ned-ordning. Varje person eller konto fortsätter längs den första vägen som matchar. Du kan ändra ordning på de definierade banorna genom att klicka på upp- och nedpilarna längst upp till höger på varje bankort för att flytta dem högre eller lägre i listan. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Läs mer</a> |
| Förbättring | Delningsnod för resa - ytterligare villkorsattribut för aktivitetshistorik | När du använder villkor för att definiera sökvägsfiltrering för en delad nod av personer finns det ytterligare två attribut: _Öppnad e-post_ och _Levererades via e-post_. Dessa tillägg ger större flexibilitet vid filtrering av personer under resan baserat på e-postaktivitet. <a href="../journeys/journey-nodes.md#split-paths">Läs mer</a> |

## Versionsinformation augusti 2024 {#Aug-2024}

**Releasedatum**: 29 augusti 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | LinkedIn-konto matchar målgrupper | Generera LinkedIn Ad-målgrupper via Account Matched Audiences för att hjälpa er att fylla tomma roller i era inköpsgrupper. Genom att definiera en uppsättning inköpsgruppfilter kan du upprätthålla en LinkedIn Matched Audience för att rikta presumtiva kunder som matchar köpgruppsparametrarna. <p>Den här funktionen utnyttjar Experience Platform Destinations för att hantera vissa aspekter av integreringen. <a href="../data/linkedin-account-matched-audiences.md">Läs mer</a> |
| Förbättring | Statuslivscykel för visuella innehållsfragment | Visuella fragment hanteras nu med en statuslivscykel. Fragmentstatusen avgör om den är tillgänglig för användning i en e-post- eller e-postmall och vilka ändringar du kan göra i den. <p>Det här förbättrade arbetsflödet gör det enkelt att hantera återanvänt innehåll enligt din kampanj- och kommunikationskalender. <a href="../content/fragments.md#fragment-status-and-lifecycle">Läs mer</a> |
