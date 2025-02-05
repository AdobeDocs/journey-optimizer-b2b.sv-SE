---
title: Versionsinformation
description: Senaste versionsinformationen för Adobe Journey Optimizer B2B-version
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 9438b1472df38eddc3e1fa6cd5bc3992af0c9eec
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 4%

---

# Versionsinformation för Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition ger kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar.

Journey Optimizer B2B edition är inbyggt i [!DNL Adobe Experience Platform] och ärver från de senaste innovationerna och förbättringarna. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest){target="_blank"}.

Granska [produktbeskrivningen](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} om du vill ha information om berättiganden, säkerhetsutkast och begränsningar.

## Versionsinformation oktober 2024 {#Oct-2024}

**Releasedatum**: 29 oktober 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | Villkorligt innehåll i e-postmallar | Anpassa ert e-postinnehåll baserat på mottagarnas beteende och profilegenskaper - både på konto- och lead-nivå. <p>När du skapar ett e-postmeddelande för din kontoresa i e-postdesignern använder du villkorliga regler för att definiera flera varianter för valfri innehållskomponent. <a href="../content/conditional-content.md">Läs mer</a> |
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
| Förbättring | Bibliotek för centrala resurser | Med det förbättrade biblioteket för _centrala resurser_ kan du använda alla bildresurser i din Marketo Engage-instans på Design Studio-arbetsytorna. Det finns inbyggda skyddsräcken som förhindrar redigering av Marketo Engage-resurser från Journey Optimizer B2B edition samt borttagnings- och flyttåtgärder. Dessa skydd säkerställer att källmaterialet (Marketo Engage Design Studio) bevaras samtidigt som det går att läsa och återanvända i Journey Optimizer B2B edition.<p>För resurser som endast är avsedda att användas i Journey Optimizer B2B edition har en specifik arbetsyta fullständiga funktioner för resurshantering. <a href="../content/marketo-engage-design-studio.md">Läs mer</a> |
| Ny funktion | Senast använda resurser | Hemsidan i Journey Optimizer B2B edition-appen innehåller nu avsnittet _[!UICONTROL Recently accessed]_, som innehåller en lista över de senast använda resurserna för marknadsföraren eller administratören. Du kan använda den här listan för att gå direkt till resursen som du nyligen arbetade med utan att navigera genom en serie resurssidor och söka. <p>Listan innehåller ytterligare information om ändringen så att du kan bestämma vilken av resurserna som behöver ändras ytterligare från det senaste mötet. För e-postresurser visas den kontoresa där e-postresursen används. <a href="../home-page.md">Läs mer</a> |
| Förbättring | Delad resenod - ändra ordning på banor | I noder med delade sökvägar utvärderas banfiltreringen i uppifrån och ned-ordning. Varje person eller konto fortsätter längs den första vägen som matchar. Du kan ändra ordning på de definierade banorna genom att klicka på upp- och nedpilarna längst upp till höger på varje bankort för att flytta dem högre eller lägre i listan. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Läs mer</a> |
| Förbättring | Delningsnod för resa - ytterligare villkorsattribut för aktivitetshistorik | När du använder villkor för att definiera sökvägsfiltrering för en delad nod av personer finns det ytterligare två attribut: _Öppnad e-post_ och _Levererades via e-post_. Dessa tillägg ger större flexibilitet vid filtrering av personer under resan baserat på e-postaktivitet. <a href="../journeys/journey-nodes.md#split-paths">Läs mer</a> |

## Versionsinformation augusti 2024 {#Aug-2024}

**Releasedatum**: 29 augusti 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Ny funktion | LinkedIn Account Matched Auditions | Generera LinkedIn Ad-målgrupper via Account Matched Audiences som hjälper er att fylla tomma roller i era inköpsgrupper. Genom att definiera en uppsättning inköpsgruppsfilter kan du upprätthålla en LinkedIn Matched Audience för att rikta presumtiva kunder som matchar era köpgruppsparametrar. <p>Den här funktionen utnyttjar Experience Platform Destinations för att hantera vissa aspekter av integreringen. <a href="../data/linkedin-account-matched-audiences.md">Läs mer</a> |
| Förbättring | Statuslivscykel för visuella innehållsfragment | Visuella fragment hanteras nu med en statuslivscykel. Fragmentstatusen avgör om den är tillgänglig för användning i en e-post- eller e-postmall och vilka ändringar du kan göra i den. <p>Det här förbättrade arbetsflödet gör det enkelt att hantera återanvänt innehåll enligt din kampanj- och kommunikationskalender. <a href="../content/fragments.md#fragment-status-and-lifecycle">Läs mer</a> |
